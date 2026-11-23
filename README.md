# Rick & Morty - Práctica con React

Aplicación web desarrollada como práctica de React para consumir una API REST y mostrar información de personajes de Rick & Morty.

## Demo

La versión publicada está disponible en:

**[https://rickandmortybyfescobar.netlify.app](https://rickandmortybyfescobar.netlify.app)**

## Funcionalidades

- Pantalla de inicio con imagen ilustrativa y botón para iniciar la búsqueda.
- Consulta de personajes a través de la **Rick and Morty API**.
- Visualización de los personajes obtenidos en una cuadrícula responsive.
- Presentación de nombre, imagen, estado, especie y cantidad de episodios de cada personaje.
- Indicador visual del estado con colores verde (`Alive`) y rojo (`Dead`).
- Navegación de vuelta a la pantalla de inicio mediante el enlace **Volver a la home**, disponible arriba y abajo del listado.

## Stack tecnológico

- **React 18** para la construcción de la interfaz basada en componentes.
- **Create React App** como entorno de desarrollo y herramienta de compilación.
- **JavaScript ES6+** y JSX.
- **React Hooks**, especialmente `useState`, para manejar el estado de la vista y los personajes obtenidos.
- **Fetch API** para realizar solicitudes HTTP a la API REST.
- **CSS3** para los estilos, la cuadrícula de personajes y el diseño responsive.
- **Testing Library** y **Jest** para pruebas de componentes.
- **Netlify** para el despliegue de la aplicación.
- **Rick and Morty API** como fuente de datos:
  [https://rickandmortyapi.com/api/character](https://rickandmortyapi.com/api/character)

## Cómo funciona

El componente `App` mantiene el listado de personajes en su estado local:

1. Al cargar la aplicación se muestra la pantalla de inicio.
2. Al presionar **Buscar Personajes**, `App` realiza una solicitud `fetch` al endpoint de personajes.
3. La respuesta JSON se transforma y guarda en el estado mediante `setCharacters`.
4. El componente `Characters` recibe la lista y genera una tarjeta por cada personaje.
5. Al seleccionar **Volver a la home**, el estado vuelve a `null` y se muestra nuevamente la vista inicial.

## Estructura del proyecto

```text
rick-and-morty-react-first-app/
├── public/
│   ├── index.html
│   ├── manifest.json
│   └── favicon.ico
├── src/
│   ├── components/
│   │   └── Characters.js
│   ├── img/
│   │   └── rick-morty.png
│   ├── App.js
│   ├── App.css
│   ├── App.test.js
│   ├── index.js
│   ├── index.css
│   ├── reportWebVitals.js
│   └── setupTests.js
├── package.json
└── package-lock.json
```

### Componentes principales

- `App`: contiene el estado principal, realiza la consulta a la API y controla si se muestran la pantalla de inicio o los personajes.
- `Characters`: recibe el listado, recorre los datos y muestra las tarjetas con la información de cada personaje.
- `App.css` e `index.css`: definen la apariencia general, los estados visuales y la adaptación a dispositivos móviles.

## Requisitos

- Node.js
- npm

## Instalación y ejecución local

Clonar el repositorio e instalar las dependencias:

```bash
npm install
```

Iniciar el servidor de desarrollo:

```bash
npm start
```

La aplicación se abrirá en [http://localhost:3000](http://localhost:3000).

## Scripts disponibles

| Comando | Descripción |
| --- | --- |
| `npm start` | Ejecuta la aplicación en modo desarrollo. |
| `npm test` | Ejecuta las pruebas en modo interactivo. |
| `npm run build` | Genera la versión optimizada de producción en la carpeta `build`. |
| `npm run eject` | Expone la configuración interna de Create React App. Es una operación irreversible. |

## Conceptos puestos en práctica

Este repositorio forma parte de una práctica de desarrollo frontend y trabaja los siguientes conceptos:

- Creación de una aplicación con Create React App.
- Organización de una interfaz en componentes.
- Uso de props y estado con `useState`.
- Consumo de APIs REST con `fetch`.
- Renderizado condicional.
- Iteración de datos con `map`.
- Uso de claves en listas de React.
- Manejo de imágenes y datos dinámicos.
- Estilos responsive con CSS y media queries.
- Preparación y despliegue de una aplicación React.
