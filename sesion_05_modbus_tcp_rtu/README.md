
# 🟦 Sesión 5 – Modbus TCP/RTU

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Programar, diagnosticar y validar la comunicación maestro-esclavo entre PLCs M580 utilizando los protocolos Modbus TCP y RTU, aplicados a entornos industriales reales.

---

## 🧭 Contenido técnico

En esta sesión se configuran dos PLCs M580 para establecer comunicación bidireccional usando Modbus, uno como maestro y otro como esclavo. Se abordarán tanto conceptos teóricos como ejercicios prácticos de conexión, lectura, escritura y manejo de errores.

- Fundamentos de Modbus TCP y RTU  
- Configuración de maestro Modbus en EcoStruxure Control Expert  
- Mapeo de direcciones y objetos (Holding Registers, Coils)  
- Configuración de esclavo Modbus RTU  
- Diagnóstico de errores: timeout, mala configuración, cables  
- Pruebas entre PLCs físicos disponibles (M580)  
- Estrategias de temporización, watchdogs y recuperación

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                           | Resultado esperado              |
|---------------|-------------------------------|-----------------------------------------------------|----------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Configuración de PLC maestro y lectura de holding registers** | Comunicación Modbus TCP validada |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Configuración de esclavo RTU, respuesta y simulación de timeout** | Prueba Modbus RTU exitosa |

---

## 📘 Recursos para la sesión

- Proyecto base con módulos NOM y configuración previa (`/recursos/proyecto_base_modbus.stu`)  
- Diagrama maestro ↔ esclavo (`/imagenes/topologia_modbus.png`)  
- Dataset de prueba (registro 40001-40010) (`/ejercicios/modbus_dataset.csv`)  
- Guía de errores típicos (`/materiales/guia_diagnostico_modbus.md`)  
- Scripts de prueba en simulador (`/ejercicios/simulador_modbus_v1.mbt`)

---

## 📝 Pasos recomendados

### 🔹 Parte A – Configuración de PLC maestro

1. Crear nueva instancia de `MODBUS_TCP_MASTER`.  
2. Asignar IP del esclavo, puerto y tiempo de ciclo.  
3. Definir operaciones: lectura de Holding Registers.  
4. Validar conexión con función de diagnóstico.  
5. Verificar datos en memoria interna (MW, %MWx).

### 🔹 Parte B – Configuración de PLC esclavo

1. Instanciar `MODBUS_TCP_SLAVE` o `MODBUS_RTU_SLAVE`.  
2. Configurar mapa de registros expuestos (coils, inputs).  
3. Simular retardo o pérdida de comunicación.  
4. Validar que el maestro detecta el error y recupera.  
5. Evaluar consistencia de datos transmitidos.

---

## 🧩 Reto 5 – Comunicación bidireccional PLC↔PLC (Modbus)

**Desafío técnico:**  
Establecer una comunicación funcional de tipo maestro ↔ esclavo entre dos PLCs M580 usando **Modbus TCP** y simular un escenario de **Modbus RTU**, con lectura y escritura exitosa.

**Entregables esperados:**

- Proyecto `.stu` maestro y esclavo con configuraciones completas  
- Captura de pantalla de diagnóstico de comunicación  
- Dataset recibido por el esclavo y mostrado en monitor  
- Reporte de prueba de fallo y recuperación  
- Archivos en carpeta `sesion_05_modbus_tcp_rtu/`

**Validación del instructor:**

- Maestro obtiene datos de esclavo sin errores  
- Respuesta RTU simulada y gestionada  
- Bitácora con evidencias de configuración y fallos diagnosticados  

---

> 💡 **Tip profesional:**  
> Conocer a profundidad el protocolo Modbus permite integrarse fácilmente con dispositivos de campo como variadores, sensores inteligentes, actuadores y SCADAs externos.
