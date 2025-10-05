# 🔄 Sesión 10 – Migración ControlWave → M580

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Convertir rutinas en Structured Text (ST) y lógica de control desarrolladas originalmente para plataformas Emerson ControlWave a una estructura estándar en PLC Schneider M580.

---

## 🧭 Contenido técnico

Los ingenieros participantes realizarán una migración controlada de un módulo típico desarrollado en RTU ControlWave a la plataforma M580, garantizando funcionalidad, organización y buenas prácticas de programación.  
Se aplicará una equivalencia lógica y estructural con enfoque en sostenibilidad, estandarización y mantenibilidad.

Este módulo es especialmente valioso considerando el plan de migración de más de **400 PLCs** en el mediano plazo.

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                        | Resultado esperado                  |
|---------------|-------------------------------|--------------------------------------------------|-------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | Adaptación de rutinas ST (ControlWave → ST M580) | Bloques migrados con lógica equivalente |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | Migración de lógicas de alarmas y válvulas       | Control migrado y probado |

---

## 🧩 Reto 10 – Módulo migrado 100% funcional

**Desafío técnico:**  
Tomar una rutina ST típica de ControlWave (por ejemplo, monitoreo de presión y apertura de válvula) y migrarla completamente al entorno de Control Expert para M580, validando equivalencias, alarmas y respuesta a fallas.

---

## 📘 Recursos entregados

- Rutinas ST de ejemplo en ControlWave (`/recursos/st_controlwave_original.txt`)
- Plantilla de migración (bloque por bloque) (`/plantillas/matriz_equivalencias_migracion.xlsx`)
- Proyecto M580 base para integración (`/proyectos/proyecto_migracion_v1.stu`)
- Manual de estilo para lógica migrada (`/guias/manual_buenas_practicas_m580.pdf`)

---

## ✅ Checklist del reto

- [ ] Rutinas ST originales comprendidas y descompuestas  
- [ ] Funcionalidad migrada en bloques DFB/FB reutilizables  
- [ ] Alarmas y condiciones límite migradas correctamente  
- [ ] Pruebas exitosas en simulador o PLC físico  
- [ ] Documentación técnica entregada en formato estándar  

---

> 💡 **Nota complementaria:**  
> Este tipo de migraciones será una de las actividades más frecuentes en los próximos años dentro del plan de transición tecnológica. Desarrollar una metodología clara y replicable desde ya, garantiza calidad, trazabilidad y agilidad para migrar múltiples estaciones.

