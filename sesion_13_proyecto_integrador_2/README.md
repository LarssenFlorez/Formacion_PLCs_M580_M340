# 🟨 Sesión 13 – Proyecto Integrador II: Implementación en PLC físico

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Descargar el proyecto integrador al PLC físico M580, validar la operación de red, la transmisión a SCADA y verificar la estabilidad completa del sistema.

---

## 🧭 Contenido técnico

En esta sesión se da el salto del entorno simulado al mundo real:  
Los ingenieros deberán desplegar el proyecto final en los **PLCs M580 físicos**, validar la comunicación con la red, los dispositivos externos y el sistema SCADA (simulado o real según disponibilidad).

Además, se revisará el desempeño de las tareas, los tiempos de respuesta, el diagnóstico de red y la operación de alarmas en condiciones reales.

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                       | Resultado esperado             |
|---------------|-------------------------------|-------------------------------------------------|--------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Descarga del proyecto y validación de ciclos de scan** | Proyecto ejecutándose en PLC físico |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Validación de red y SCADA + diagnóstico**       | Proyecto operativo y estable   |

---

## 🧩 Reto 13 – Proyecto final físico con protocolos activos

**Desafío técnico:**  
Implementar y validar un sistema que esté ejecutándose en hardware real, incluyendo los 3 protocolos (Modbus, Profinet, DNP3), alarmas activas, diagnósticos funcionales y documentación completa.

---

## 📘 Recursos entregados

- Proyecto final validado para hardware (`/proyectos/final_fisico_v1.stu`)  
- Checklist de validación física (`/plantillas/validacion_en_plc.xlsx`)  
- Procedimiento de descarga y verificación (`/guías/descarga_control_expert.pdf`)  
- Plantilla de reporte final (`/documentos/reporte_final_operacion.docx`)

---

## ✅ Checklist del reto

- [ ] Proyecto descargado sin errores  
- [ ] Módulos E/S respondiendo correctamente  
- [ ] Red estable entre PLCs (Profinet)  
- [ ] Comunicación activa vía Modbus y DNP3  
- [ ] Alarmas funcionando en tiempo real  
- [ ] Reporte técnico diligenciado y entregado  

---

## 🔁 Paso a paso recomendado

1. **Conectar el PC al PLC físico (puerto de programación / red).**

2. **Verificar dirección IP del PLC y configuración de red.**

3. **Cargar el proyecto final desde Control Expert.**  
   Confirmar ausencia de errores en la compilación.

4. **Iniciar la operación del PLC (RUN) y validar LEDs de diagnóstico.**

5. **Ejecutar pruebas de lectura/escritura en E/S físicas.**

6. **Verificar comunicación con dispositivos externos por Profinet y Modbus.**

7. **Asegurar que las señales llegan al SCADA vía DNP3 (si canal habilitado).**

8. **Revisar alarmas y buffers desde interfaz local y Wireshark.**

9. **Documentar resultados en la plantilla de validación física.**

10. **Subir el proyecto, bitácora y reporte técnico al repositorio GitHub.**

---

> 💡 **Nota importante:**  
> Esta sesión representa una validación final del conocimiento adquirido y la capacidad de ejecutar un proyecto profesional. El enfoque está en **autonomía técnica**, **diagnóstico** y **entregables documentados** que sirvan de base para futuros despliegues.

