# 🟥 Sesión 8 – DNP3 I: Fundamentos y configuración esclavo

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Configurar un PLC M580 como esclavo DNP3, validar la calidad de datos y los timestamps con un simulador SCADA.

---

## 🧭 Contenido técnico

Esta sesión introduce de forma práctica el protocolo **DNP3 (Distributed Network Protocol)** en el contexto de automatización industrial, particularmente en entornos donde los datos deben transmitirse de forma confiable y estructurada a sistemas SCADA.

- Fundamentos del protocolo DNP3: estructura, objetos y variaciones
- Configuración del PLC como esclavo DNP3
- Definición de puntos (analógicos, digitales, binarios) y clases
- Creación de ASDU y su asociación con señales
- Validación de calidad, timestamps y eventos
- Verificación de tramas con simulador de SCADA (Spectrum Power 7 o equivalente)

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                | Resultado esperado                  |
|---------------|-------------------------------|------------------------------------------|-------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Configuración de objetos y ASDU en esclavo DNP3** | PLC esclavo respondiendo peticiones |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Validación de eventos, calidad y timestamp**      | Tramas monitoreadas y verificadas   |

---

## 📘 Recursos para la sesión

- Proyecto base con módulo DNP3 (`/recursos/proyecto_dnp3_base.stu`)  
- Manual Schneider – Configuración DNP3 (`/materiales/manual_dnp3_schneider.pdf`)  
- Herramienta de simulación SCADA o Spectrum Power 7 (acceso restringido)  
- Plantilla de mapeo de objetos y ASDU (`/plantillas/mapeo_dnp3.xlsx`)  
- Capturador de tramas (Wireshark con filtros preconfigurados)

---

## 📝 Pasos recomendados

### 🔹 Parte A – Configuración como esclavo

1. Habilitar protocolo DNP3 en la configuración del PLC (M580)  
2. Definir el rango de objetos digitales y analógicos (p. ej., 30.1, 30.2)  
3. Asociar cada señal con su ASDU correspondiente  
4. Establecer el ID del esclavo y puerto de escucha (TCP o serie)  
5. Cargar proyecto al PLC y esperar solicitud del maestro

### 🔹 Parte B – Validación con simulador

1. Configurar maestro DNP3 en herramienta de simulación  
2. Consultar señales de forma cíclica o por evento  
3. Verificar timestamps y calidad de datos en cada respuesta  
4. Identificar códigos de error si los hay  
5. Guardar captura de tramas para análisis posterior

---

## 🧩 Reto 8 – Esclavo DNP3 operativo y verificado

**Desafío técnico:**  
Dejar el PLC M580 completamente operativo como **esclavo DNP3**, con objetos correctamente mapeados, calidad verificada y tramas validadas con simulador SCADA.

**Entregables esperados:**

- Proyecto .stu funcional con configuración DNP3 esclavo  
- Captura de pantalla del simulador leyendo datos correctamente  
- Captura Wireshark de tramas con timestamps válidos  
- Documento PDF con tabla de objetos configurados y su clase

**Validación del instructor:**

- PLC responde correctamente ante lectura o evento desde maestro  
- Calidad y timestamps son consistentes  
- Configuración clara y documentación entregada en el repositorio del grupo

---

> 💡 **Tip profesional:**  
> DNP3 es el protocolo más usado en sistemas SCADA modernos. Dominar su configuración, interpretación y diagnóstico te permitirá implementar proyectos en sistemas críticos como energía, agua o gas.

