# Integrate MCP with Copilot

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey Andeveling!

Mona here. I'm done preparing your exercise. Hope you enjoy! 💚

## Project Overview
Este proyecto es una aplicación web basada en FastAPI para gestionar y apuntarse a actividades extracurriculares. El objetivo es aprender a expandir las capacidades de GitHub Copilot usando Model Context Protocol (MCP).

## Getting Started

1. Instala las dependencias:
   ```sh
   pip install -r requirements.txt
   ```
2. Ejecuta la aplicación:
   ```sh
   uvicorn src.app:app --reload
   ```
3. Abre tu navegador en:
   - Documentación interactiva: http://localhost:8000/docs
   - Documentación alternativa: http://localhost:8000/redoc
   - Sitio web estático: http://localhost:8000/static/

## API Endpoints
| Método | Endpoint                                                          | Descripción                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Lista todas las actividades y participantes actuales                |
| POST   | `/activities/{activity_name}/signup?email=tu@email.com`           | Apunta a un estudiante a una actividad                              |

## Data Model
- **Actividades:** Identificadas por nombre, incluyen descripción, horario, máximo de participantes y lista de emails inscritos.
- **Estudiantes:** Identificados por email.
- Todos los datos se almacenan en memoria (se reinician al reiniciar el servidor).

## Ejercicio y Flujos Automatizados
- El avance del ejercicio y la retroalimentación se gestionan mediante GitHub Actions y comentarios en Issues.
- Puedes consultar el progreso y los siguientes pasos en los Issues del repositorio.

---
&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

