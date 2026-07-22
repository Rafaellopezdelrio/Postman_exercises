# Postman_exercises

Ejercicios de **testing de APIs REST con Postman**: colecciones con peticiones y
validaciones automáticas sobre APIs públicas.

## Colecciones

| Archivo | API | Sobre qué es |
|---|---|---|
| `ChuckNorrisApi.postman_collection.json` | [Chuck Norris API](https://api.chucknorris.io) | API pública de frases, con categorías y búsqueda |
| `Rick&MortyApi.postman_collection.json` | [Rick and Morty API](https://rickandmortyapi.com) | API pública con personajes, episodios y localizaciones (respuestas paginadas) |

## Qué se valida

- Códigos de estado de la respuesta (200, 404…)
- Estructura y contenido del cuerpo JSON
- Comportamiento de los distintos endpoints de cada API

## Cómo usarlo

**Desde Postman**
1. *Import* → seleccionar el archivo `.json` de la colección
2. Abrir la colección y lanzar las peticiones
3. Pestaña *Test Results* para ver el resultado de las validaciones
4. O ejecutar toda la colección con el **Collection Runner**

**Desde consola con Newman**
```bash
npm install -g newman
newman run ChuckNorrisApi.postman_collection.json
newman run "Rick&MortyApi.postman_collection.json"
```

## Qué he practicado

- Construcción de peticiones REST y lectura de respuestas JSON
- Scripts de test en Postman para automatizar las validaciones
- Organización de peticiones en colecciones reutilizables
- Ejecución por línea de comandos con Newman (integrable en CI)
