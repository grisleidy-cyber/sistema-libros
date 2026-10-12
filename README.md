# 📚 Sistema de Libros — CRUD en la nube

Aplicación web para administrar el catálogo de una biblioteca, desarrollada para la actividad **Despliegue de un sistema CRUD en la nube** (Cloud Computing, Unidad 2).

## Tecnologías

| Componente   | Tecnología                     |
| ------------ | ------------------------------ |
| Interfaz     | React + Vite                   |
| API REST     | Node.js (Netlify Functions)    |
| Base de datos| Google Sheets (Google Sheets API) |
| Repositorio  | GitHub                         |
| Despliegue   | Netlify                        |

## Arquitectura

```
Usuario → React (Netlify) → API REST (Netlify Functions) → Google Sheets
```

## Funcionalidades

- Login básico (usuario/contraseña).
- CRUD completo de libros: título, autor, categoría, año y ejemplares.
- Búsqueda por título o autor, filtro por categoría y contador de registros.
- Validación de formularios y confirmación antes de eliminar.
- Diseño responsivo.

## API

| Método | Ruta                              | Acción             |
| ------ | --------------------------------- | ------------------ |
| GET    | `/.netlify/functions/libros`      | Consultar libros   |
| POST   | `/.netlify/functions/libros`      | Crear libro        |
| PUT    | `/.netlify/functions/libros/:id`  | Actualizar libro   |
| DELETE | `/.netlify/functions/libros/:id`  | Eliminar libro     |

## Variables de entorno

Copia `.env.example` a `.env` y completa los valores (nunca subas `.env` al repositorio):

- `SHEET_ID`
- `GOOGLE_CLIENT_EMAIL`
- `GOOGLE_PRIVATE_KEY`

## Ejecutar localmente

```bash
npm install
npx netlify-cli dev
```
