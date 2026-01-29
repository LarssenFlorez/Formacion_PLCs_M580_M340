# 🟩 Sesión 4 – Carga Masiva de Señales CSV

**Duración:** 4.5 horas (7:30 a.m. – 12:00 m)  
**Objetivo:** Automatizar la creación y vinculación de tags mediante archivos CSV estructurados, reduciendo errores y mejorando la eficiencia en la programación de proyectos con altos volúmenes de señales.

---

## 🧭 Contenido técnico

Esta sesión explora el uso avanzado del asistente de importación/exportación de variables en **EcoStruxure Control Expert** usando archivos `.CSV`. Aprenderás a construir archivos validados con múltiples señales analógicas y digitales, y vincularlas directamente a bloques funcionales.

- Estructura de archivos `.CSV` para Control Expert  
- Reglas de nomenclatura y consistencia  
- Validación previa con Excel   
- Importación de tags al proyecto  
- Corrección de errores frecuentes (espacios, formatos, celdas vacías, duplicados)


---

## ⚙️ Agenda y actividades

| Horario       | Grupo                         | Actividad                                  | Resultado esperado                      |
|---------------|-------------------------------|--------------------------------------------|------------------------------------------|
| 7:30 – 9:45   | Grupo 1-2 (PLC #1) / Grupo 3-4 (PLC #2) | **Generación y validación de CSV (50+ tags)** | Archivo estructurado y libre de errores |
| 10:00 – 12:00 | Grupo 3-4 (PLC #1) / Grupo 1-2 (PLC #2) | **Importación al proyecto** | Proyecto operativo con todas las señales cargadas |

---

## 📘 Recursos para la sesión

- Plantilla CSV con formato correcto (`/recursos/plantilla_csv_tanque.csv`)  
- Proyecto de Sesión 3 con DFBs cargados (`/recursos/proyecto_con_libreria.stu`)  
- Hoja de validación rápida (`/materiales/checklist_validacion_csv.xlsx`)  
- Carpeta `/imagenes/` para capturas de prueba y validación

---

## 📝 Pasos recomendados

### 🔹 Parte A – Generación y validación de CSV

1. Abrir plantilla base con 50 señales predefinidas.  
2. Asignar nombres, tipos, comentarios y direcciones.  
3. Validar sintaxis en Excel.
4. Probar importación en proyecto.
5. Revisar errores y corregir conflictos de duplicados o tipo de dato.

### 🔹 Parte B – Importación al proyecto y vinculación

1. Importar el archivo CSV al proyecto real.  
2. Verificar carga correcta en `Variables → Variables del proyecto`.  
3. Asignar señales a bloques funcionales creados previamente.  
4. Ejecutar simulación para comprobar funcionamiento.  
5. Guardar copia del proyecto con CSV integrado.

---

## 🧩 Reto 4 – Tags importados y funcionando en menos de 15 minutos

**Desafío técnico:**  
Importar y vincular más de 50 señales al proyecto funcional en **menos de 15 minutos**, sin errores en nombres, tipos ni direcciones.

**Entregables esperados:**

- Archivo `.CSV` validado y funcional  
- Proyecto `.stu` con variables activas  
- Capturas o evidencias del funcionamiento  
- Subida al repositorio: `sesion_04_integracion_csv/`  

**Validación del instructor:**

- Proyecto funcional sin errores de compilación  
- Todas las señales conectadas a bloques  
- Revisión de la bitácora del grupo con pasos y errores encontrados

---

> 💡 **Tip profesional:**  
> El dominio de carga masiva por CSV es una habilidad clave para proyectos reales con cientos de señales. Automatizar hoy significa escalar mañana.

