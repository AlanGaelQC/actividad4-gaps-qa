Va, le subo el nivel visual pero sin inventar nada (los números y links siguen siendo los reales que ya corrimos):

markdown
# 🧪 Actividad 4 — Gestión y Automatización de Pruebas de Software

> Pipeline completo de pruebas de API: manual → automatizado → mockeado → corriendo solo en cada push.

![API Tests](https://github.com/AlanGaelQC/actividad4-gaps-qa/actions/workflows/newman.yml/badge.svg)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-orange?style=flat)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![JWT](https://img.shields.io/badge/Auth-JWT-black?style=flat&logo=jsonwebtokens)

---

## 🚀 Qué hace este proyecto

Una API REST completa (mockeada), probada de punta a punta y verificada automáticamente en cada cambio — sin intervención manual:

| Capa | Herramienta | Qué prueba |
|---|---|---|
| 🌐 API | [MockAPI.io](https://6aa21355ccb3db9689a606ce.mockapi.io/api/products) | CRUD completo sobre `products` |
| 🔐 Auth | [DummyJSON](https://dummyjson.com/auth/login) | Login JWT + petición autenticada |
| ✅ Tests | Postman (Tests tab) | Status code, body, headers |
| 🎭 Mocking | Postman Mock Server | Escenarios 200 / 404 simulados |
| ⚙️ CI/CD | GitHub Actions + Newman | Corre todo, en cada `push` |

## 📊 Resultado de la última corrida

requests: 10/10 executed, 0 failed
assertions: 25/25 executed, 0 failed


## 📁 Estructura

.
├── postman/
│ ├── Actividad4 - Products API.postman_collection.json
│ └── Actividad4.postman_environment.json
└── .github/
└── workflows/
└── newman.yml


## ▶️ Correrlo en local

```bash
npm install -g newman
newman run "postman/Actividad4 - Products API.postman_collection.json" -e "postman/Actividad4.postman_environment.json"
```

## 🧠 Lo que se puso a prueba

- ✅ 4 métodos HTTP (GET, POST, PUT, DELETE) con validaciones automáticas
- ✅ Autenticación por token, guardado en variables de entorno — nunca hardcodeado
- ✅ Mocking de respuestas de éxito y error sin depender del backend real
- ✅ Pipeline que se rompe si algo se rompe — cero pruebas manuales en producción

---
🎓 **Curso:** Gestión y Automatización de Pruebas de Software — Tecmilenio****
