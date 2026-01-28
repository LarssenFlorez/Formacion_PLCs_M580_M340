# 🟨 Sesión 3 – Diseño de Librerías DFB/FB

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Crear bloques reutilizables, documentados y versionados usando estructuras de programación estandarizadas en EcoStruxure Control Expert Classic.

---

## 🧭 Contenido técnico

Esta sesión se centra en el diseño profesional de **librerías de bloques funcionales (DFB/FB)** que puedan ser integradas a cualquier proyecto de forma escalable y mantenible.

- Creación de bloques analógicos estándar (ej. DFB_AnalogInput).  
- Diseño de bloques digitales combinados (DFB_DigitalIO).
- diseño de bloque de manejo dde alarmas (DFB_AlarmManager)   
- Definición de parámetros, comentarios y versiones.  
- Validación funcional en simulador y/o PLC físico.


---

## ⚙️ Agenda y actividades

| Horario         | Grupo        | Actividad                          | Resultado esperado                          |
|-----------------|--------------|------------------------------------|---------------------------------------------|
| 7:30 – 9:45     | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Diseño de bloque DFB_AnalogInput** | Bloque operativo con entradas, salida, comentarios y versión |
| 10:00 – 12:00   | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Diseño de DFB_DigitalIO + AlarmManager** | Librería consolidada, probada e integrada |

---

## 📘 Recursos para la sesión

- Proyecto base de Sesión 2 (`/recursos/proyecto_avanzado.stu`)  
- Guía de diseño de DFBs (`/materiales/guia_bloques_dfb.pdf`)  
- Carpeta `/ejercicios/` con ejemplos de bloques previos.  
- Carpeta `/imagenes/` para evidencias y capturas.
- Generador de señales Fluke para prueba de señales analógicas.

---

## 📝 Pasos recomendados

### 🔹 Parte A – DFB_AnalogInput
1. Crear nuevo bloque DFB con nombre estandarizado.  
2. Definir entradas: canal, valor, span, cero.  
3. Crear lógica de escala + saturación + diagnóstico.  
4. Documentar internamente cada línea del bloque.  
5. Guardar versión 1.0 y probar en PLC o simulador.

### 🔹 Parte B – DFB_DigitalIO y AlarmManager
1. Crear DFB para entrada/salida digital (1 entrada, 1 salida).  
2. Agregar parámetros de activación manual y lógica inversa.  
3. Diseñar bloque AlarmManager básico (detección + reset).  
4. Probar secuencias de activación y validación de alarmas.  
5. Integrar bloques a librería y exportar `.XDB`.

---

## 🧩 Reto 3 – Librería DFB/FB documentada y subida

**Meta:** Tener una librería completa con al menos 3 bloques funcionales, cada uno:
- Comentado.
- Estandarizado.
- Versionado.

**Entregables:**
- Archivo `.STU` con librería integrada.  
- README con descripción de bloques y parámetros.  
- Evidencias de prueba funcional.  
- Carga al repositorio en carpeta `sesion_03_librerias_dfb_fb`.

**Validación del instructor:**
- Bloques cumplen estructura técnica y funcional.  
- Están integrados al proyecto base de sesiones anteriores.  
- Se identifican versiones y autores de cada bloque.

---

> 💡 **Consejo:**  
> Una librería bien hecha no es solo funcional, es transferible. Que otro ingeniero pueda entenderla sin tu ayuda es la verdadera prueba de calidad.
