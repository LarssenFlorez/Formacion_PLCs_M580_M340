# 🟦 Sesión 2 – Programación Avanzada IEC 61131-3  

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** desarrollar lógica combinada en **LD**, **ST** y **FBD** con multitareas y buenas prácticas de programación estructurada.  

---

## 🧭 Contenido técnico

Esta sesión está enfocada en **pasar de la configuración base a la programación avanzada**, utilizando los lenguajes IEC 61131-3 dentro de EcoStruxure Control Expert:

- Diseño de rutinas principales y secundarias en **LD (Ladder Diagram)**.  
- Implementación de bloques analógicos y digitales en **FBD (Function Block Diagram)**.  
- Uso de **ST (Structured Text)** para cálculos y control avanzado.  
- Documentación clara de bloques y variables.  


---

## ⚙️ Agenda y actividades

| Horario | Grupo | Tema / Actividad | Objetivo de aprendizaje |
|---------|--------|------------------|-------------------------|
| 7:30 – 9:45 (2h15) | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Rutina principal y módulos de entrada digital** | Lógica determinística implementada y comentada |
| 10:00 – 12:00 (2h) | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Programación en ST y bloques análogos en FBD** | Rutinas combinadas + test unitario en PLC físico |

---

## 📘 Recursos para la sesión

- Proyecto base de la Sesión 1 (`/recursos/plantilla_proyecto_base.ZEF`).   
- Carpeta `/imagenes/` para diagramas y ejemplos.  

---

## 📝 Pasos recomendados

### 🔹 Parte A (7:30 – 9:45)
1. Abrir proyecto base de Sesión 1.  
2. Crear **tarea MAIN_DIGITAL**.  
3. Programar entradas digitales en **LD** (ej: %I0.0.0 → %Q0.0.0) O (ej: %M100.0 → %Q0.0.0).  
4. Documentar bloques y variables según estándar.  
5. Compilar y descargar al PLC.  
<img width="1423" height="357" alt="image" src="https://github.com/user-attachments/assets/f41c36ee-81dd-4ab9-96ef-0dde86bee07d" />


### 🔹 Parte B (10:00 – 12:00)
1. Crear **tarea ANALOG**.  
2. Programar bloques de lectura analógica en **FBD**.  
3. Implementar cálculos en **ST** (por ejemplo, conversión de mA a unidades de ingeniería).  
4. Realizar test unitario en PLC físico y capturar evidencias.  
5. Subir cambios al repositorio GitHub en carpeta `Sesion_02`.
<img width="1198" height="573" alt="image" src="https://github.com/user-attachments/assets/6012fdfc-6fd7-4b21-ac4b-c00757f47e39" />
<img width="1682" height="740" alt="image" src="https://github.com/user-attachments/assets/40b91f4d-2d96-48d7-b1b0-d0d25a56977d" />


---

## 🧩 Reto 2 – Lógica sincronizada multitarea funcional

**Meta:** tener la lógica digital y analógica funcionando de forma sincronizada en dos tareas separadas.

**Entregables:**
- Proyecto `.ZEF o .STU` con:
  - Tareas MAIN_DIGITAL y ANALOG creadas.
  - Bloques LD/FBD/ST funcionales.
- Lista de variables actualizada en `.csv`.
- Evidencias de pruebas en PLC físico (capturas en `/imagenes/`).
- README en carpeta `Sesion_02` con breve descripción del avance.

**Validación del instructor:**
- Lógica determinística sin errores de compilación.
- Rutinas comentadas y estandarizadas.
- Test unitario documentado en GitHub.

---

> 💡 **Consejo:**  
> Para cálculos analógicos usar **Structured Text (ST)** con funciones propias. Esto les permitirá aplicar lógica compleja de forma más eficiente y reutilizable.

