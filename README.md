# mycoolhistory.app

A web application that analyses your browser history and classifies visited sites into topics using a machine-learning model.

## Technologies Used

### Frontend
| Technology | Purpose |
|---|---|
| [React 19](https://react.dev/) | UI component library |
| [Vite](https://vitejs.dev/) | Build tool & development server |
| [React Router v7](https://reactrouter.com/) | Client-side routing |
| [Tailwind CSS v4](https://tailwindcss.com/) | Utility-first CSS framework |
| [Cytoscape.js](https://js.cytoscape.org/) / [react-cytoscapejs](https://github.com/plotly/react-cytoscapejs) | Graph visualisation |
| [react-force-graph](https://github.com/vasturiano/react-force-graph) / [D3-force](https://github.com/d3/d3-force) | Force-directed graph layout |
| [Lucide React](https://lucide.dev/) | Icon set |

### Backend
| Technology | Purpose |
|---|---|
| [Java 21](https://openjdk.org/projects/jdk/21/) | Runtime language |
| [Spring Boot 4](https://spring.io/projects/spring-boot) | Application framework |
| [Spring Data JPA](https://spring.io/projects/spring-data-jpa) | ORM / database access layer |
| [Maven](https://maven.apache.org/) | Build & dependency management |

### Machine-Learning Service
| Technology | Purpose |
|---|---|
| [Python](https://www.python.org/) | Runtime language |
| [FastAPI](https://fastapi.tiangolo.com/) | REST API framework |
| [Uvicorn](https://www.uvicorn.org/) | ASGI server |
| [PyTorch](https://pytorch.org/) | Deep-learning backend |
| [sentence-transformers](https://www.sbert.net/) (`all-MiniLM-L6-v2`) | Text embeddings for topic classification |
| [scikit-learn](https://scikit-learn.org/) | Feature normalisation |
| [pandas](https://pandas.pydata.org/) / [NumPy](https://numpy.org/) | Data processing |

### Database
| Technology | Purpose |
|---|---|
| [PostgreSQL](https://www.postgresql.org/) (Alpine image) | Persistent relational storage |

### Infrastructure
| Technology | Purpose |
|---|---|
| [Docker](https://www.docker.com/) | Containerisation |
| [Docker Compose](https://docs.docker.com/compose/) | Multi-container orchestration |

## Architecture Overview

```
Browser
  └─► Frontend  (React/Vite · port 5173)
        └─► Backend  (Spring Boot · port 8080)
              ├─► PostgreSQL  (port 5432)
              └─► ML Service  (FastAPI · port 8000)
```

## Getting Started

```bash
docker compose up --build
```

The frontend will be available at <http://localhost:5173>.
