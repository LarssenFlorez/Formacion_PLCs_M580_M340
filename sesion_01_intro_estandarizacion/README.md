# 🟩 Sesión 1 – Introducción, Arquitectura y Estandarización de Proyectos  

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** establecer la estructura base del curso, reconocer la arquitectura de los PLC M580/M340 y crear el primer proyecto funcional estandarizado.

---

## 🧭 Contenido técnico

### 1️⃣ Introducción general al ecosistema Schneider

**EcoStruxure Control Expert** es la plataforma de ingeniería para programar y configurar los controladores **Modicon** (M340, M580, M251, etc.), ofreciendo un entorno compatible con IEC 61131-3.

Durante esta sesión se revisará:
- **Arquitectura M340:**  
  - PLC modular compacto, orientado a control local.  
  - CPU principales: BMXP34xxx con módulos E/S analógicos y digitales.  
  - Comunicación: Ethernet, Modbus, CANopen.
- **Arquitectura M580:**  
  - PLC de alto desempeño con CPU ePAC (Ethernet Programmable Automation Controller).  
  - CPU BMEP58xxxx con bus Ethernet nativo.  
  - Comunicación integrada: Modbus TCP, Profinet, DNP3, OPC UA.  
  - Módulos típicos:  
    | Tipo | Modelo | Descripción |
    |------|---------|-------------|
    | Fuente | **BMXCPS3500** | 24V DC, 3.5A |
    | CPU | **BMEP581020** | CPU Ethernet, 2 puertos RJ45 |
    | Comunicación | **BMXNOM0200** | Serial RS232/485 |
    | Comunicación Ethernet | **BMXNOR0200H** | 2 puertos RJ45 TCP/IP |
    | Bastidor | **BMXXBP0600** | 6 ranuras |

💡 *Durante el curso se trabajará con 2 PLC M580 completos y simulaciones equivalentes en Control Expert.*

---

## ⚙️ Actividades prácticas

| Actividad | Descripción | Tiempo |
|------------|--------------|--------|
| Introducción y objetivos | Contexto del curso, explicación de arquitectura y módulos | 1h |
| Creación de proyecto base | Configuración CPU, bastidor y red | 1.5h |
| Creación de tarea MAIN y test de comunicación | Lógica simple + compilación | 1h |
| Documentación y sincronización en GitHub | Carga del proyecto base | 1h |

---

## ⚙️ Creación del proyecto base paso a paso

### 🔹 Paso 1 – Crear un nuevo proyecto
1. Abrir **EcoStruxure Control Expert**.  
2. Ir a `File → New Project`.  
3. Seleccionar:  
   - **Family:** Modicon M580
   - Seleccionar la CPU con la que se va a trabajar
4. Confirmar con **OK**.
<img width="1091" height="580" alt="image" src="https://github.com/user-attachments/assets/ba2c1649-9fa0-4ad1-8aa2-6e1d8036b5c1" />

---

### 🔹 Paso 2 – Configurar el bastidor y la CPU
1. En el panel izquierdo (Project Browser), dar clic derecho en `Rack 0 → Insert Module` o doble click.  
2. Agregar los siguientes módulos en orden:
   - ** Validar la fuente preseleccionada poir el software y dado caso cambiarla por la que se tenga fisicamente**  en nuestro caso BMXCPS3500.
   - Validar el Firmware de la CPU
   - **Slot 2:** BMXNOM0200 (Serial)  
   - **Slot 3:** BMXNOR0200H (Ethernet)
3. Compilar la configuracion.

<img width="1092" height="577" alt="image" src="https://github.com/user-attachments/assets/c300641f-6c80-468f-b4d2-1de18ff67498" />


---

### 🔹 Paso 3 – Configurar la red Ethernet
1. Seleccionar (doble click) los puerto RJ45 de la CPU para abrir → pestaña **Ethernet**.  
2. Asignar una IP local (por ejemplo):
   192.168.10.10
   Subnet mask: 255.255.255.0
3. Aplicar cambios y guardar.
<img width="1091" height="576" alt="image" src="https://github.com/user-attachments/assets/6c756c00-5d87-4b95-a228-09551246ddaf" />

---

### 🔹 Paso 4 – Crear una tarea cíclica (MAIN)
1. En el árbol del proyecto, expandir `Program → Tasks  → Logic`.
2. Clic derecho → **Logic**.
   <img width="1091" height="522" alt="image" src="https://github.com/user-attachments/assets/88928141-f2f6-47a4-9786-06b4a2324c57" />  
4. Asignar nombre:
   MAIN_TASK
5. Dentro de la tarea, crear un **POU (Program Organization Unit)**:
- Tipo: **LD (Ladder Diagram)**  
- Nombre: `MAIN`  
- Agregar una instrucción para test:
  ```
  %Q0.0 := %I0.0;
  ```
  <img width="1088" height="515" alt="image" src="https://github.com/user-attachments/assets/d47b1ebe-d97d-40f9-9eae-575b84d4ade6" />
  
  (entrada digital reflejada en salida digital)

  <img width="595" height="473" alt="image" src="https://github.com/user-attachments/assets/0166ae90-d56b-402d-ad7a-6df74105c591" />

  🧩 1. I/O data type: Topological

🔹 Significado:
Indica que las variables de entrada/salida se asignarán automáticamente según la dirección física (topológica) del módulo en el chasis.

🔹 Cómo funciona:
Cada canal del módulo se direcciona directamente en base a su slot y posición dentro del bastidor.
Por ejemplo:

%I0.1.0 → Entrada digital 0 del módulo en el slot 1
%Q0.2.3 → Salida digital 3 del módulo en el slot 2


🧩 2. I/O data type: Device DDT

🔹 Significado:
Crea una estructura de datos (DDT - Derived Data Type) para el módulo completo.
En lugar de direccionar cada canal manualmente, el software genera una variable compuesta con nombres legibles y campos automáticos (por ejemplo Module_x.CH0, Module_x.Fault, Module_x.Status, etc.).

🔹 Cómo funciona:
Cuando seleccionas esta opción, Control Expert crea una variable estructurada:

Module_DI_1602 : BMX_DDI_1602


Y dentro de ella puedes acceder a los canales:

Module_DI_1602.CH0.Value
Module_DI_1602.CH1.Value
Module_DI_1602.Diag
Module_DI_1602.ChannelFault

---

### 🔹 Paso 5 – Compilar y simular
1. Clic en **Build (F9)** → verificar que no existan errores.  
2. Activar el **Simulador** (`Alt + F7`).  
3. Forzar entradas (%I) y verificar salidas (%Q).  

💡 Si se dispone del PLC físico, conectar el cable Ethernet y probar conexión directa (`PLC → Connect → Login`).

---

## 🧩 Estructura del proyecto estándar

Todos los proyectos del curso deberán mantener esta organización:

- MAIN
- INIT (Inicialización de variables)
- LOGIC (Rutinas principales)
- ALARMS (Bloques de alarmas)
- COMMS (Protocolos de comunicación)
- UTILITIES (Funciones y librerías)

---

## 🧩 Reto 1 – Proyecto Base Documentado

**Meta:** crear un proyecto completamente funcional y documentado en ambos PLCs.

**Entregables:**
- Proyecto `.zrx` operativo (CPU + módulos configurados).  
- Captura de conexión exitosa con PLC físico o simulador.  
- Carpeta `Sesion_01` actualizada en el repositorio GitHub.  

**Validación del instructor:**
- Proyecto compila y comunica correctamente.  
- Nomenclatura y comentarios correctos.  
- Sincronización exitosa entre PLC1 y PLC2.  

---

> 💡 **Consejo:**  
> Cada grupo (1-2 / 3-4) debe dejar una *bitácora de traspaso* en el repositorio (`handover_s01.txt`) indicando las configuraciones y observaciones realizadas.








