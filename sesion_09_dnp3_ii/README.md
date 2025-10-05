# 🟥 Sesión 9 – DNP3 II: Integración con SCADA SP7 y diagnóstico

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Validar la comunicación DNP3 entre PLC M580 (esclavo) y SCADA Siemens SP7 (maestro), analizando buffers, clases y calidad de datos.

---

## 🧭 Contenido técnico

En esta sesión se realiza una integración práctica entre el PLC M580 configurado como esclavo DNP3 y el SCADA **Spectrum Power 7** (SP7) operado por EPM.  
Aunque no se tiene acceso directo a la configuración del SCADA, se trabajará bajo un escenario real de campo donde los ingenieros deberán:

- Asegurar que el PLC está correctamente parametrizado como esclavo  
- Solicitar al área SCADA la creación del canal maestro en SP7  
- Probar y validar la transmisión de datos a través del canal  
- Usar Wireshark para auditar y diagnosticar la calidad de la comunicación  

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                      | Resultado esperado                 |
|---------------|-------------------------------|------------------------------------------------|------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Preparación del canal DNP3 y activación de señales** | PLC esclavo operativo con objetos mapeados |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Captura y análisis de buffers con Wireshark** | Comunicación validada y documentada |

---

## 🧩 Reto 9 – Transmisión AI/DI con calidad validada

**Desafío técnico:**  
Simular un escenario real donde el PLC M580 funcione como esclavo DNP3 ante un sistema SCADA externo. Se debe asegurar que las señales se transmiten correctamente y auditar las tramas usando herramientas como **Wireshark**.

---

## 📘 Recursos entregados

- Proyecto base del PLC como esclavo (`/recursos/proyecto_dnp3_esclavo_v2.stu`)  
- Plantilla de solicitud de canal DNP3 para SCADA SP7 (`/documentos/solicitud_canal_dnp3_sp7.docx`)  
- Librería de objetos DNP3 (`/librerias/dfb_dnp3_2024.lib`)  
- Guía rápida para verificación de tramas en Wireshark (`/guías/wireshark_dnp3_basico.pdf`)

---

## ✅ Checklist del reto

- [ ] PLC M580 configurado como esclavo con objetos válidos  
- [ ] Solicitud de canal enviada al área SCADA  
- [ ] Confirmación de recepción desde SP7  
- [ ] Captura de tramas DNP3 con Wireshark  
- [ ] Análisis: calidad, timestamps, eventos y buffers  
- [ ] Reporte técnico con evidencias y conclusiones

---

## 🔁 Paso a paso recomendado

1. **Cargar el proyecto base al PLC físico o simulador.**  
   Asegúrate de que la configuración del CPU y red sea coherente con las pruebas.

2. **Configurar los objetos DNP3 esclavo en Control Expert.**  
   Define las clases, objetos, variaciones y atributos con ASDU.

3. **Verificar parámetros clave (dirección, puerto, calidad de datos).**  
   Revisa que el PLC esté preparado para recibir conexión externa.

4. **Preparar la plantilla de solicitud del canal DNP3 para SP7.**  
   Incluye información técnica clara y completa: IP, ASDU, puertos, lista de puntos.

5. **Enviar la solicitud al equipo SCADA de EPM.**  
   (En el escenario real, este paso debe hacerse con antelación).

6. **Solicitar prueba de conexión desde el SP7 al PLC.**  
   Espera confirmación de que el maestro ha iniciado la consulta.

7. **Capturar las tramas de red usando Wireshark.**  
   Filtra por puerto DNP3 y verifica handshake, requests y responses.

8. **Analizar buffers y calidad de datos.**  
   Verifica si las clases configuradas son correctas, si los eventos llegan con timestamp y si hay errores.

9. **Elaborar reporte técnico final.**  
   Incluye capturas, análisis de buffers, evidencia de puntos leídos y sugerencias si algo falló.

---

> 💡 **Nota importante:**  
> Esta simulación se alinea con escenarios reales donde los ingenieros no tienen acceso al SCADA, pero deben asegurar que su equipo esté correctamente configurado y sea visible para sistemas maestros. Esta habilidad es esencial para la migración futura de más de 400 PLCs.
