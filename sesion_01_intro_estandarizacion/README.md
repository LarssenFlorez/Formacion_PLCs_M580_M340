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

## ⚙️ Creación del proyecto base paso a paso

### 🔹 Paso 1 – Crear un nuevo proyecto
1. Abrir **EcoStruxure Control Expert**.  
2. Ir a `File → New Project`.  
3. Seleccionar:  
   - **Family:** Modicon M580  
   - **Template:** “Empty Project”  
   - Asignar nombre:  
     ```
     M580_S01_BASE_[INICIALES]
     ```
4. Confirmar con **OK**.

---

### 🔹 Paso 2 – Configurar el bastidor y la CPU
1. En el panel izquierdo (Project Browser), dar clic derecho en `Rack 0 → Insert Module`.  
2. Agregar los siguientes módulos en orden:
   - **Slot 0:** BMEP581020 (CPU)  
   - **Slot 1:** BMXCPS3500 (Power Supply)  
   - **Slot 2:** BMXNOM0200 (Serial)  
   - **Slot 3:** BMXNOR0200H (Ethernet)
3. Verificar que todos los módulos aparezcan **en verde (OK)** en el diagrama.

---

### 🔹 Paso 3 – Configurar la red Ethernet
1. Seleccionar el módulo **BMXNOR0200H** → pestaña **Ethernet**.  
2. Asignar una IP local (por ejemplo):
   192.168.10.10
   Subnet mask: 255.255.255.0
3. Aplicar cambios y guardar.

---

### 🔹 Paso 4 – Crear una tarea cíclica (MAIN)
1. En el árbol del proyecto, expandir `Program → Tasks`.  
2. Clic derecho → **New Periodic Task**.  
3. Asignar nombre:
   MAIN_TASK
   Cycle time: 100 ms
4. Dentro de la tarea, crear un **POU (Program Organization Unit)**:
- Tipo: **LD (Ladder Diagram)**  
- Nombre: `MAIN`  
- Agregar una simple instrucción para test:
  ```
  %Q0.0 := %I0.0;
  ```
  (entrada digital reflejada en salida digital)

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

## ⚙️ Actividades prácticas

| Actividad | Descripción | Tiempo |
|------------|--------------|--------|
| Introducción y objetivos | Contexto del curso, explicación de arquitectura y módulos | 1h |
| Creación de proyecto base | Configuración CPU, bastidor y red | 1.5h |
| Creación de tarea MAIN y test de comunicación | Lógica simple + compilación | 1h |
| Documentación y sincronización en GitHub | Carga del proyecto base | 1h |

---

## 🧩 Reto 1 – Proyecto Base Documentado

**Meta:** crear un proyecto completamente funcional y documentado en ambos PLCs.

**Entregables:**
- Proyecto `.zrx` operativo (CPU + módulos configurados).  
- Captura de conexión exitosa con PLC físico o simulador.  
- Archivo CSV con variables iniciales (`tags_base.csv`).  
- Carpeta `Sesion_01` actualizada en el repositorio GitHub.  

**Validación del instructor:**
- Proyecto compila y comunica correctamente.  
- Nomenclatura y comentarios correctos.  
- Sincronización exitosa entre PLC1 y PLC2.  

---

> 💡 **Consejo:**  
> Cada grupo (1-2 / 3-4) debe dejar una *bitácora de traspaso* en el repositorio (`handover_s01.txt`) indicando las configuraciones y observaciones realizadas.








