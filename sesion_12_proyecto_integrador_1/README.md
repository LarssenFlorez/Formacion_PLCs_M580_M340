# 🟪 Sesión 12 – Proyecto Integrador I

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Integrar en un solo proyecto los protocolos y configuraciones trabajadas en sesiones anteriores: **Modbus**, **Profinet** y **DNP3**, simulando un sistema completo con alarmas, señales, librerías y diagnóstico.

---

## 🧭 Contenido técnico

Esta sesión marca el inicio del **Proyecto Integrador**, en el que los participantes deberán consolidar todo lo aprendido hasta ahora en un solo proyecto unificado, orientado a una aplicación real.

Durante la sesión, se integrará la comunicación simultánea con dispositivos Modbus (actuadores), una red Profinet entre PLCs, y la salida de señales hacia un SCADA por DNP3.  
Además, se configurará la gestión de alarmas críticas y diagnósticos básicos para cada protocolo, incluyendo estrategias de fallback y detección de fallos.

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                    | Resultado esperado                  |
|---------------|-------------------------------|----------------------------------------------|-------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Integración de protocolos: Modbus + Profinet + DNP3** | Proyecto unificado funcional        |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Configuración de alarmas y diagnóstico básico** | Sistema completo en simulador activo |

---

## 🧩 Reto 12 – Proyecto integrador en simulador operativo

**Desafío técnico:**  
Lograr que el proyecto sea capaz de comunicarse por **3 protocolos industriales simultáneamente**, responda a eventos en tiempo real y genere alarmas coherentes en el simulador.  

Este reto es el punto de partida para las pruebas finales con hardware físico.

---

## 📘 Recursos entregados

- Proyecto base para integración (`/proyectos/integrador_v1.stu`)  
- Librerías DFB/FB completas (`/librerías/paquete_completo_2024.lib`)  
- Plantilla de validación de alarmas y comunicación (`/plantillas/integrador_checklist.xlsx`)  
- Simulador de fallos para red y protocolos (`/simuladores/falla_multicanal.exe`)  
- Documento técnico de arquitectura recomendada (`/documentos/arquitectura_proyecto_integrador.pdf`)

---

## ✅ Checklist del reto

- [ ] Modbus TCP operativo con lectura/escritura  
- [ ] Red Profinet estable y diagnosticada  
- [ ] Salida DNP3 hacia canal simulado validada  
- [ ] Alarmas integradas y visualizadas  
- [ ] Diagnóstico básico en tramas o tags  
- [ ] Simulación del sistema completa y documentada  

---

## 🔁 Paso a paso recomendado

1. **Importar el proyecto base integrador al software EcoStruxure Control Expert.**

2. **Configurar el módulo Modbus TCP para lectura de variables externas.**  
   Validar holding registers, tiempo de respuesta, y retries.

3. **Configurar el canal Profinet entre los dos PLC.**  
   Verificar direcciones IP, roles y disponibilidad.

4. **Configurar salida esclava DNP3.**  
   Asegurar que los objetos y clases estén correctamente definidos.

5. **Diseñar y cargar una rutina de alarmas globales.**  
   Activar por condiciones críticas (fallo, comunicación, rebose, etc.)

6. **Probar el sistema completo en simulador.**  
   Validar que las señales fluyen por los 3 canales sin colisiones ni pérdida.

7. **Diligenciar la plantilla de validación.**  
   Documentar tiempos, eventos, alarmas y observaciones.

8. **Subir la evidencia al repositorio GitHub.**  
   Incluye capturas, grabaciones, proyecto .STU y checklist final.

---

> 💡 **Nota importante:**  
> Este módulo prepara al grupo para pasar a pruebas con PLC físico en la siguiente sesión. Es fundamental asegurar que toda la lógica, comunicación y alarmas estén probadas antes de subir al hardware real.

