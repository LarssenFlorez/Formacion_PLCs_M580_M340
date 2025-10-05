# 🟥 Sesión 9 – DNP3 II: Integración con Spectrum Power 7 y diagnóstico

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Establecer comunicación PLC ↔ SCADA utilizando DNP3 y analizar buffers, clases y eventos en tramas capturadas.

---

## 🧭 Contenido técnico

En esta sesión se consolidan los conocimientos de DNP3 integrando el PLC M580 con un sistema SCADA real (Spectrum Power 7), y se analizan las clases, eventos y buffers transmitidos para validar la calidad de datos y comportamiento del protocolo.

- Configuración del maestro DNP3 en Spectrum Power 7
- Asociación de señales analógicas y digitales en SCADA
- Validación de clases 0, 1, 2 y 3
- Interpretación de buffers, timestamps y eventos
- Captura y análisis de tramas con Wireshark
- Estrategias de optimización de transmisión

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                      | Resultado esperado                 |
|---------------|-------------------------------|------------------------------------------------|------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Configuración completa en SCADA SP7 como maestro** | Comunicación establecida con el PLC |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Análisis de tramas: clases, eventos, calidad**     | Reporte técnico validado con capturas |

---

## 📘 Recursos para la sesión

- Proyecto DNP3 esclavo del PLC M580 (`/recursos/proyecto_dnp3_esclavo.stu`)  
- Configuración SCADA SP7 para prueba (`/recursos/sp7_dnp3_config.json`)  
- Manual técnico de DNP3 para SCADA Siemens  
- Plantilla de análisis de tramas (`/plantillas/dnp3_buffers_wireshark.xlsx`)  
- Capturador de tráfico (Wireshark) con filtros DNP3

---

## 📝 Pasos recomendados

### 🔹 Parte A – Configuración con SP7

1. Ingresar a Spectrum Power 7 y abrir el módulo de configuración DNP3  
2. Crear canal maestro y asociar el PLC como esclavo con dirección IP y puerto  
3. Mapear variables analógicas y digitales desde la tabla del PLC  
4. Habilitar polling cíclico y reporte por evento  
5. Confirmar recepción correcta de AI, DI y eventos en tiempo real

### 🔹 Parte B – Análisis con Wireshark

1. Capturar tráfico entre SCADA y PLC durante prueba  
2. Filtrar por `dnp3` y revisar contenido de tramas  
3. Validar clases (0, 1, 2, 3), timestamps y buffers  
4. Identificar problemas de retraso, pérdida o mal mapeo  
5. Guardar evidencia y documentar los hallazgos

---

## 🧩 Reto 9 – Transmisión AI/DI con calidad validada

**Desafío técnico:**  
Demostrar una comunicación robusta entre el PLC M580 y SCADA SP7 con señales analógicas y digitales correctamente transmitidas, con calidad, timestamps y eventos consistentes.

**Entregables esperados:**

- Captura de pantalla de SP7 mostrando las señales activas  
- Captura Wireshark con clases diferenciadas y sin errores  
- Proyecto .stu ajustado con objetos correctos  
- Documento PDF resumen con análisis de la comunicación y su calidad

**Validación del instructor:**

- Todas las señales visibles en SP7 con calidad buena  
- Tramas en Wireshark completas, sin repetición errónea  
- Timestamps consistentes con los eventos en el PLC

---

> 💡 **Tip profesional:**  
> La integración con SCADA en campo depende no solo del protocolo, sino de la correcta gestión de buffers y clases. Un sistema bien afinado minimiza retrasos y mejora la confiabilidad del proceso.

