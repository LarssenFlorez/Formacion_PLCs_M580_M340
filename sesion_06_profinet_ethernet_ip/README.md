# 🟦 Sesión 6 – Profinet / Ethernet IP

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Implementar topologías de red industrial robustas para M580 usando Profinet o Ethernet/IP y realizar diagnóstico detallado con herramientas de monitoreo como Wireshark.

---

## 🧭 Contenido técnico

En esta sesión se abordará la integración de los PLCs a redes Ethernet industriales, el direccionamiento de dispositivos, la validación de conectividad y el análisis de tráfico en tiempo real. Se busca fortalecer la capacidad de diagnóstico de los ingenieros en redes críticas.

- Fundamentos de Profinet y Ethernet/IP en M580  
- Configuración de interfaces de red y direccionamiento IP  
- Topologías recomendadas: línea, anillo, estrella  
- Configuración de puertos, VLAN y segmentación básica  
- Captura y análisis de paquetes con Wireshark  
- Identificación de latencias, errores y pérdidas  
- Estrategias de diagnóstico proactivo

---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                             | Resultado esperado          |
|---------------|-------------------------------|---------------------------------------|------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Topología física y asignación de IPs** | PLC en red estable y direccionado |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Captura y diagnóstico de paquetes con Wireshark** | Tráfico analizado y explicado |

---

## 📘 Recursos para la sesión

- Proyecto base con puertos habilitados (`/recursos/proyecto_redes.stu`)  
- Archivo con esquema de red para la sesión (`/imagenes/topologia_redes.png`)  
- Guía rápida de Wireshark (`/materiales/wireshark_basico.pdf`)  
- Plantilla de asignación IP (`/plantillas/asignacion_ips.xlsx`)  
- Script de prueba de latencia (`/ejercicios/ping_script.bat`)  

---

## 📝 Pasos recomendados

### 🔹 Parte A – Configuración de red

1. Definir IPs para cada PLC (ej. 192.168.1.10 y 192.168.1.20).  
2. Configurar interface de red en Control Expert.  
3. Conectar ambos PLCs mediante switch y verificar comunicación.  
4. Ejecutar prueba de ping y registrar tiempos.  
5. Subir proyecto actualizado al repositorio.

### 🔹 Parte B – Diagnóstico con Wireshark

1. Iniciar captura en el adaptador de red correspondiente.  
2. Generar tráfico entre PLCs (lectura de variables).  
3. Filtrar por protocolo (`profinet` o `ethernet/ip`).  
4. Analizar latencia, errores, pérdidas o desconexiones.  
5. Guardar y documentar la captura (`.pcap`).

---

## 🧩 Reto 6 – Red activa y diagnosticada por ambos equipos

**Desafío técnico:**  
Configurar una red funcional entre los dos PLCs y capturar, interpretar y documentar al menos 3 eventos de tráfico relevantes (ej. conexión, latencia, retransmisión).

**Entregables esperados:**

- Proyecto con configuración de red  
- Captura de pantalla del diagnóstico desde Control Expert  
- Archivo `.pcap` con tráfico registrado  
- Plantilla de análisis completada  
- Bitácora con hallazgos y evidencias

**Validación del instructor:**

- Dirección IP correcta y funcional en ambos PLCs  
- Wireshark utilizado con filtros adecuados  
- Identificación y explicación de al menos un comportamiento de red (delay, error, retry)

---

> 💡 **Tip profesional:**  
> Una red bien segmentada y diagnosticada no solo mejora el rendimiento del sistema, sino que previene fallos costosos. Aprender a interpretar Wireshark es una habilidad crítica para cualquier ingeniero de automatización moderna.

