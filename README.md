# InventaMX: Sistema POS & Inventario Offline-First

![Status](https://img.shields.io/badge/Status-Fase%200%3A%20Ideaci%C3%B3n-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Methodology](https://img.shields.io/badge/Methodology-Agile%20%2F%20GitHub%20Flow-orange)

> **Transformando la gestión de micro-comercios en México mediante tecnología accesible.**

## Sobre el Proyecto
**InventaMX** es una Progressive Web App (PWA) diseñada para resolver los problemas críticos de los pequeños abarrotes en zonas con conectividad intermitente. El proyecto simula un entorno real de ingeniería de software, enfocándose en la **Calidad**, **Escalabilidad** y **Experiencia de Usuario (UX)**.

El cliente piloto es "Abarrotes Doña Lucha", permitiendo validar hipótesis con datos reales del mercado mexicano.

---

## Metodología y Filosofía de Trabajo

Este proyecto no es solo código; es un ejercicio de **Ingeniería de Software**. Se rige por los siguientes principios:

### 1. Estrategia MVP (Producto Mínimo Viable)
Siguiendo la metodología **Lean Startup**, no buscamos construir un ERP masivo desde el día 1.
* **Enfoque:** Resolver el "Dolor #1" del usuario (Tiempos de cobro y Falta de stock).
* **Alcance v1.0:** Venta rápida + Control de inventario local + Modo Offline.
* **Exclusiones:** Facturación SAT y Pagos con tarjeta (pospuestos para Fase 2).
* **Objetivo:** Validar la adopción del usuario antes de invertir en funcionalidades complejas.

### 2. Gobernanza del Código (GitHub Flow)
Utilizamos una estrategia de ramas moderna y ágil, evitando la burocracia de *Gitflow* tradicional:
* **`main`**: Es nuestra única fuente de verdad. Siempre desplegable (Production Ready).
* **Feature Branches**: Todo cambio vive en una rama efímera (`feat/...`, `docs/...`).
* **Branch Protection**:
    * No se permiten commits directos a `main`.
    * Todo cambio requiere un **Pull Request (PR)**.
    * Las pruebas (CI) deben pasar antes de fusionar.

### 3. Gestión Ágil (Kanban)
Gestionamos el flujo de trabajo mediante **GitHub Projects**:
* **Issues:** Cada tarea es un ticket con criterios de aceptación claros.
* **Milestones:** Agrupamos tareas por Fases del SDLC (Ideación, Diseño, Desarrollo, Despliegue).
* **Etiquetas Semánticas:** Uso estricto de labels (`P0: Critical`, `type: bug`, `type: feat`) para priorización.

---

## Estructura del Repositorio
El proyecto sigue una estructura documental alineada al ciclo de vida del software:

* `Fase_0_Ideacion_Gobernanza/`: Project Charter, Lean Canvas y Actas.
* `Fase_1_Requerimientos/`: Historias de Usuario y Backlog (Próximamente).
* `src/`: Código fuente de la aplicación (Próximamente).

---

## 🛠️ Stack Tecnológico (Preliminar)
* **Frontend:** React + Vite (PWA)
* **Backend:** Supabase (Backend-as-a-Service)
* **CI/CD:** GitHub Actions + Vercel
* **Testing:** Vitest + Playwright

---
*Desarrollado con por Carlos Saúl Arenas Maciel como Portafolio Profesional.*