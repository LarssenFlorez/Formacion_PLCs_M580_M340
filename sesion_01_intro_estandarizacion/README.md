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
