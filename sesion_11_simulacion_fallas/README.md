# 🟦 Sesión 11 – Simulación y Pruebas de Falla

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Evaluar la resiliencia del sistema ante fallas de red y energía, verificando la capacidad de recuperación automática del proyecto programado en M580.

---

## 🧭 Contenido técnico

En esta sesión los participantes se enfrentarán a **escenarios simulados de falla**, tanto a nivel de red de comunicación como de corte de energía, buscando validar que el sistema está correctamente preparado para **detectar, actuar y recuperarse** ante estas situaciones.

Se trabajará sobre el proyecto completo desarrollado hasta la sesión anterior, enfocándose en:

- El comportamiento de las tareas cíclicas ante interrupciones
- La robustez de la programación frente a fallas intermitentes
- La correcta restauración del proyecto tras pérdida de energía
- Estrategias prácticas de diagnóstico, logs y alarmas

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                         | Resultado esperado              |
|---------------|-------------------------------|-----------------------------------|---------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Simulación de falla de red y pruebas de reconexión** | Reconexión automática verificada |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Simulación de corte de energía y recuperación del sistema** | Proyecto funcional tras reinicio |

---

## 🧩 Reto 11 – Proyecto restaurado y documentado

**Desafío técnico:**  
Forzar situaciones reales de fallo (desconexión de red, corte de energía) y validar que el sistema sea capaz de **recuperarse automáticamente sin perder datos críticos** ni entrar en estados inconsistentes.

Los equipos deberán entregar una documentación que evidencie los tiempos de recuperación, las acciones tomadas por el sistema, y cómo se configuraron las variables persistentes o las estrategias de restauración.

---

## 📘 Recursos entregados

- Proyecto base actualizado con backup (`/proyectos/m580_backup_v3.stu`)  
- Guía de simulación de fallas de red (`/guías/falla_red.pdf`)  
- Plantilla de pruebas de corte de energía (`/plantillas/corte_energia_checklist.xlsx`)  
- Documento de mejores prácticas de resiliencia (`/documentos/resiliencia_plc_industrial.pdf`)

---

## ✅ Checklist del reto

- [ ] Proyecto funcional antes de la prueba  
- [ ] Red simulada con pérdida y reconexión  
- [ ] Corte eléctrico simulado en PLC físico  
- [ ] Restauración completa del sistema  
- [ ] Validación de reinicio sin pérdida de datos  
- [ ] Documento técnico con evidencias y lecciones aprendidas  

---

## 🔁 Paso a paso recomendado

1. **Verificar que el proyecto cargado esté operativo en ambos PLC.**  
   Asegúrate de que todas las señales estén actualizadas y comunicando correctamente.

2. **Simular falla de red (desconectar físicamente o desde switch).**  
   Observa el comportamiento del sistema, tiempos de espera, alarmas activadas, y recuperación.

3. **Documentar comportamiento durante la desconexión y reconexión.**  
   ¿El PLC logra mantener coherencia en variables? ¿Se reconecta automáticamente?

4. **Simular corte de energía (desconectar alimentación del PLC).**  
   Aplica solo si se puede realizar de forma segura. Alternativamente, usar el simulador para reiniciar el CPU.

5. **Verificar el comportamiento del proyecto al reiniciar.**  
   Comprobar si retoma las tareas, reinicia en estado seguro o presenta errores.

6. **Validar la persistencia de variables si aplica.**  
   Revisar si las configuraciones o estados previos al corte se mantienen.

7. **Completar la plantilla de análisis de fallos.**  
   Incluir tiempos medidos, alarmas activadas, variables impactadas y tiempo de recuperación.

8. **Subir evidencia al repositorio.**  
   Capturas de pantalla, grabaciones, archivos de proyecto y checklist diligenciado.

---

> 💡 **Nota:**  
> Esta sesión es clave para asegurar que los ingenieros sean capaces de diseñar y mantener sistemas **resilientes**, preparados para escenarios reales de desconexiones intermitentes o fallos eléctricos, tan comunes en campo.

