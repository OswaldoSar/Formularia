# Formulario SISCO para GitHub Pages

Formulario web profesional y responsivo del **Inventario SISCO del Estrés Académico (31 ítems)**.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html`.
3. En GitHub entra a **Settings > Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`.
6. Guarda los cambios.

## Guardar respuestas

El formulario viene en **modo demostración**. Si no configuras un backend, al finalizar descargará la respuesta como `.json`.

Para recibir respuestas en línea, abre `index.html` y busca:

```js
const SUBMIT_ENDPOINT = "";
```

Reemplaza el valor por la URL de tu endpoint, por ejemplo un Web App de Google Apps Script.

### Formato enviado

Se envía un `POST` con JSON con esta estructura aproximada:

```json
{
  "edad": "16",
  "sexo": "Femenino",
  "grado": "5.º de secundaria",
  "seccion": "A",
  "q1": "Sí",
  "q2": "4",
  "q3": "3",
  "...": "...",
  "q31": "4",
  "otra_estresor": "",
  "otra_comportamental": "",
  "otra_afrontamiento": "",
  "timestamp": "2026-10-02T16:00:00.000Z"
}
```

## Funcionalidades incluidas

- Diseño profesional y adaptable a celular.
- Barra de progreso.
- Validación de preguntas obligatorias.
- Filtro del ítem 1: si la respuesta es "No", no se muestran los demás ítems.
- Escalas Likert visuales.
- Campos opcionales “Otra (especifique)”.
- Preparado para GitHub Pages.
- Preparado para conectar con Google Apps Script, Formspree u otro backend.
