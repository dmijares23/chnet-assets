# chnet-assets

Este repositorio contiene archivos JSON estructurados con datos utilizados en el ecosistema **ChircalNet**. Incluye información sobre colores, modelos de vehículos y configuraciones específicas de red.

---

## 📁 Archivos disponibles

### [`colors.json`](https://raw.githubusercontent.com/dmijares23/chnet-assets/main/colors.json)
Contiene una lista de colores definidos por nombre y su valor hexadecimal. Útil para temas de UI o selección de color.

```json
[
  { "name": "Rojo", "hex": "#FF0000" },
  { "name": "Verde", "hex": "#00FF00" },
  { "name": "Azul", "hex": "#0000FF" }
  // ...
]
```

---

### [`models.json`](https://raw.githubusercontent.com/dmijares23/chnet-assets/main/models.json)
Define marcas de vehículos y sus respectivos modelos. Ideal para formularios, filtros y autocompletado.

```json
[
  {
    "id": 1,
    "nombre": "Audi",
    "modelos": ["A5", "A3", "A4", "Q5", "Q7"]
  },
  {
    "id": 2,
    "nombre": "BMW",
    "modelos": ["Serie 1", "Serie 3", "X1", "X3"]
  }
  // ...
]
```

---

### [`chircalnet.json`](https://raw.githubusercontent.com/dmijares23/chnet-assets/main/chircalnet.json)
Contiene datos específicos de configuración y topología de red utilizados por la infraestructura de **ChircalNet**. Incluye nodos, rutas y otras propiedades relevantes para monitoreo y planificación.

> ℹ️ Debido a su tamaño, se recomienda cargar este archivo dinámicamente desde el frontend/backend o analizarlo parcialmente.

---

## 📦 Cómo usar estos archivos

Puedes acceder a estos archivos desde cualquier entorno que permita llamadas HTTP (JavaScript, Python, etc.).

### Ejemplo en JavaScript

```ts
async function loadJSON(url) {
  const response = await fetch(url);
  return await response.json();
}

const colors = await loadJSON('https://raw.githubusercontent.com/dmijares23/chnet-assets/main/colors.json');
const models = await loadJSON('https://raw.githubusercontent.com/dmijares23/chnet-assets/main/models.json');
const chircalnet = await loadJSON('https://raw.githubusercontent.com/dmijares23/chnet-assets/main/chircalnet.json');
```

### Descarga por terminal

```bash
curl -O https://raw.githubusercontent.com/dmijares23/chnet-assets/main/colors.json
curl -O https://raw.githubusercontent.com/dmijares23/chnet-assets/main/models.json
curl -O https://raw.githubusercontent.com/dmijares23/chnet-assets/main/chircalnet.json
```

---

## 🛠 Contribuciones

¿Deseas agregar más marcas, colores u otros datos? ¡Eres bienvenido!  
Haz un fork, edita y abre un pull request.

---

## 📄 Licencia

Este repositorio está bajo la licencia [MIT](LICENSE).
