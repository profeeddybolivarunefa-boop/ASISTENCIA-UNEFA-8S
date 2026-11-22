# Sistema de Control de Asistencia — Defensa Integral de la Nación VIII (UNEFA)

Aplicación web estática desarrollada para la gestión, validación y consolidación de asistencia de los estudiantes de la asignatura **Defensa Integral de la Nación VIII**, unificando las secciones **08S-2422-D1** y **08S-2622-D1** bajo la titularidad del **Prof. Eddy Alexander Bolívar Rodríguez**.

---

## Características Principales

* **Unificación de Secciones:** Consolida en un único padrón oficial a los 70 estudiantes inscritos (40 de la sección `08S-2422-D1` y 30 de la sección `08S-2622-D1`).
* **Ventana Emergente de Captura (`Popup`):** Interfaz modal con el encabezado *"Ingresar cédula o escanear cédula"* diseñada para lectura continua mediante escáner de código de barras/QR o ingreso manual por teclado.
* **Control Antiduplicados:** Verifica en tiempo real si la cédula ya fue registrada en la sesión activa, bloqueando cualquier intento de doble registro y emitiendo una alerta visual inmediata.
* **Persistencia Local (`LocalStorage`):** Conserva automáticamente los registros de asistencia en el navegador del dispositivo para evitar pérdida de datos ante recargas accidentales.
* **Totalización Automática:** Calcula al pie del acta el total de personal convocado, total de asistentes, total de inasistentes y porcentajes discriminados por sección y total general.
* **Exportación a PDF en 1 Sola Hoja:** Genera el acta oficial en formato Carta vertical ajustada estrictamente a una página, lista para firma y entrega administrativa.

---

## Estructura del Repositorio

```text
/
├── index.html      # Aplicación principal (interfaz, padrón unificado, lógica de escaneo y exportación PDF)
├── README.md       # Documentación técnica y guía de uso del repositorio
└── .nojekyll       # Archivo marcador para desactivar el procesamiento Jekyll en GitHub Pages
```

---

## Despliegue en GitHub Pages

1. Verifique que los archivos `index.html`, `README.md` y `.nojekyll` se encuentren en la raíz de la rama principal (`main` o `master`).
2. En el repositorio de GitHub, diríjase a **Settings** > **Pages**.
3. En la sección **Build and deployment**, seleccione:
   * **Source:** `Deploy from a branch`
   * **Branch:** `main` (o `master`) y carpeta `/ (root)`
4. Haga clic en **Save** y espere unos segundos hasta que GitHub Pages publique la dirección web (`https://<usuario>.github.io/<nombre-repositorio>/`).

---

## Uso Operativo en Aula o Campo

1. Abra el enlace publicado desde su computadora o teléfono móvil.
2. En la ventana emergente **"Ingresar cédula o escanear cédula"**, pase el lector óptico o digite el número de cédula (con o sin prefijo `V-`) y presione `Enter`.
3. Al finalizar el pase de lista, cierre la ventana emergente y haga clic en **"Descargar Acta en PDF (1 Hoja)"** para obtener el reporte oficial listo para imprimir o compartir.