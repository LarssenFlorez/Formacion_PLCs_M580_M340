# 🟪 Sesión 7 – Profibus DP

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Integrar dispositivos esclavos Profibus DP al PLC M580, validar la red y registrar diagnósticos de fallas.

---

## 🧭 Contenido técnico

En esta sesión se trabajará con la configuración de redes **Profibus DP**, su estructura jerárquica, y el diagnóstico en tiempo real de su estado. Se busca formar competencias clave para identificar fallos comunes y documentar adecuadamente la salud del bus.

- Fundamentos de Profibus DP (topología, velocidad, direccionamiento)
- Configuración del maestro DP en M580 (con módulo NOR0200H)
- Integración de dispositivos esclavos (ej. módulos de E/S o simulados)
- Lectura de datos y monitoreo de estado de red
- Interpretación de códigos de error, pérdidas de comunicación y alarmas de red
- Bitácora técnica de eventos, fallas y mantenimientos recomendados

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                | Resultado esperado                 |
|---------------|-------------------------------|------------------------------------------|------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Configuración del maestro DP y esclavos simulados** | Red Profibus activa sin errores     |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Lectura de diagnóstico y bitácora de fallos**     | Documento con errores detectados   |

---

## 📘 Recursos para la sesión

- Proyecto base con módulo NOR configurado (`/recursos/profibus_base.stu`)  
- Archivo GSD de dispositivo esclavo simulado (`/recursos/device_profibus.gsd`)  
- Guía rápida de códigos de error Profibus (`/materiales/codigos_error_profibus.pdf`)  
- Plantilla para bitácora de red (`/plantillas/bitacora_red_profibus.xlsx`)  
- Topología sugerida de conexión (`/imagenes/topologia_profibus.png`)  

---

## 📝 Pasos recomendados

### 🔹 Parte A – Configuración inicial

1. Agregar módulo maestro Profibus DP al rack virtual (NOR0200H).  
2. Importar GSD del dispositivo esclavo (o simulado).  
3. Asignar dirección y configurar velocidad del bus.  
4. Conectar dispositivo (simulado o real) a la red.  
5. Validar comunicación y tabla de entrada/salida.

### 🔹 Parte B – Diagnóstico y documentación

1. Provocar desconexión o error en el esclavo.  
2. Verificar alarma en Control Expert y variable de diagnóstico.  
3. Capturar código de error y buscar en tabla de referencia.  
4. Registrar evento en plantilla de bitácora.  
5. Subir reporte al repositorio del grupo.

---

## 🧩 Reto 7 – Profibus DP funcional y documentado

**Desafío técnico:**  
Implementar comunicación estable entre maestro-esclavo Profibus y registrar, interpretar y documentar al menos un fallo simulado.

**Entregables esperados:**

- Proyecto .stu funcional con red Profibus activa  
- Captura de pantalla de comunicación activa  
- Bitácora de al menos un evento de error documentado  
- Archivo `.pdf` con resumen de diagnóstico y solución aplicada

**Validación del instructor:**

- Red operativa con al menos un esclavo conectado  
- Bitácora clara con código de error y solución tentativa  
- Conclusión técnica sobre la estabilidad de la red

---

> 💡 **Tip profesional:**  
> Profibus DP sigue siendo ampliamente usado en la industria. Saber diagnosticarlo correctamente marca la diferencia entre un técnico operativo y un ingeniero experto.

