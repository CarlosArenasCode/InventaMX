# Problem Statement: InventaMX

## Información General
| Campo | Detalle |
|-------|---------|
| **ID del Proyecto** | PORTFOLIO-2026-001 |
| **Nombre del Proyecto** | Sistema de Inventario y POS "InventaMX" |
| **Fecha de Creación** | 2026-01-31 |
| **Versión** | 1.0 |
| **Autor** | Carlos Saúl Arenas Maciel |
| **Sponsor** | Sra. Elena Martínez, Dueña de "Abarrotes Doña Lucha" (PyME simulada con 2 empleados) |
| **Stakeholders Clave** | Dueños de microtiendas (Admin), Empleados de mostrador (Vendedor) |

---

## Declaración del Problema

> *"Los dueños de microtiendas en México (abarrotes, ferreterías, misceláneas) experimentan **pérdidas no cuantificadas de $2,500–$6,000 MXN mensuales** al gestionar inventarios y ventas con libretas o memoria, resultando en stockouts no detectados, merma no registrada y cierres de caja que consumen 45–60 minutos diarios en negocios con ventas promedio de $35,000 MXN/mes."*

---

## Impacto Cuantificable Actual

| Métrica | Situación Actual (Manual/Libreta) | Meta con InventaMX | Brecha (Gap) |
|---------|-----------------------------------|--------------------|--------------|
| **Tiempo de corte de caja** | 45-60 min diarios (cuadrar libreta vs dinero) | ≤ 5 min diarios (automático) | Ahorro de ~50 min/día |
| **Ventas perdidas por falta de stock** | 15% de las solicitudes de clientes | ≤ 3% | Recuperación de 12 pp de venta |
| **Detección de robo hormiga/merma** | Imposible de rastrear (desconocido) | Trazabilidad por turno/usuario | Visibilidad 100% |
| **Curva de aprendizaje empleado** | 2 semanas (memorizar precios) | < 15 minutos (sistema visual/búsqueda) | Reducción drástica |

---

## Alcance del Problema

- **Contexto estadístico real**:
  - México tiene **~605,000 tiendas de abarrotes registradas** según el Directorio Estadístico Nacional de Unidades Económicas (DENUE) del INEGI.
  - El **43% de las empresas pierde dinero por mala gestión de inventarios** según CANACO CDMX (2025).
  - El **98.7% de los negocios en México son micro, pequeñas y medianas empresas**, predominando el comercio minorista.

- **Áreas afectadas**: Mostrador (Ventas), Almacén (Inventario), Administración (Finanzas básicas).
- **Personas impactadas**: 
  - *El Dueño*: Vive estresado, no puede dejar el negocio solo, desconoce su ganancia real.
  - *El Empleado*: Comete errores de cobro por cálculo mental, sufre desconfianza del dueño.
- **Procesos críticos afectados**:
  - Registro de venta rápida (fila de clientes esperando).
  - Reabastecimiento (saber qué comprar al proveedor).
  - Detección de caducidad o merma.

---

## Objetivo de la Solución Propuesta

Desarrollar un MVP (Producto Mínimo Viable) de software web/móvil que:
1. **Digitalice** el inventario y las ventas con interfaz intuitiva para usuarios no técnicos (alfabetización digital equivalente a WhatsApp).
2. **Centralice** la información en la nube para que el dueño monitoree el negocio remotamente desde su smartphone.
3. **Optimice costos** usando hardware existente (smartphone/tablet con cámara) sin requerir escáneres USB o terminales costosas.

---

## Criterios de Éxito (KPIs Separados)

### KPIs de Negocio
| KPI | Situación Actual | Meta con InventaMX | Medición |
|-----|------------------|--------------------|----------|
| Tiempo de corte de caja | 45–60 min/día | ≤ 5 min/día | Cronometrado en 5 días consecutivos |
| Ventas perdidas por stockout | 15% de solicitudes | ≤ 3% | Reporte de productos agotados vs. solicitudes |
| Error en cobro | ~8% de transacciones | < 0.5% | Conciliación caja vs. sistema |
| Satisfacción usuario (NPS) | N/A (no medido) | ≥ 70/100 | Encuesta post-uso simulada |

### KPIs Técnicos
| KPI | Meta | Medición |
|-----|------|----------|
| Tiempo de registro de venta | < 10 segundos | Pruebas en dispositivo gama media (Redmi A2) |
| Disponibilidad del sistema | 99.5% uptime | UptimeRobot primer mes post-lanzamiento |
| Tamaño de bundle frontend | ≤ 1.5 MB | Lighthouse Audit |
| Soporte offline básico | Sincronización automática al recuperar conexión | Pruebas de desconexión/reconexión |

---

## Riesgos Iniciales Identificados

| Riesgo | Probabilidad | Impacto | Mitigación Propuesta |
|--------|--------------|---------|----------------------|
| Resistencia al cambio (dueños prefieren libreta física) | Alta | Alto | Diseñar flujo que simule libreta (ej.: botón "Anotar venta" con icono de lápiz) + onboarding < 3 minutos |
| Conectividad intermitente en zonas populares | Media | Alto | Arquitectura offline-first con IndexedDB + sincronización automática al recuperar señal |
| Error humano en digitación de precios/productos | Media | Medio | Validación visual + confirmación en 2 pasos para precios > $500 MXN |
| Abandono por curva de aprendizaje | Baja | Alto | Tutoriales contextuales (tooltips) + soporte por WhatsApp simulado |

---

## Supuestos y Limitaciones (Contexto MVP)

| Tipo | Descripción |
|------|-------------|
| **Supuestos** | - El usuario final cuenta con smartphone con navegador web y conexión a internet intermitente.<br>- El usuario tiene alfabetización digital básica (usa WhatsApp, Facebook). |
| **Limitaciones** | - No incluye integración con facturación electrónica (SAT) en esta fase.<br>- No soporta escáneres USB (solo cámara del dispositivo para códigos de barras). |
| **Restricciones** | - **Presupuesto**: $0.00 MXN (herramientas Free Tier únicamente).<br>- **Equipo**: 1 desarrollador fullstack.<br>- **Tiempo**: 6 semanas para versión Beta funcional. |

---

## Próximos Pasos (Fase 0: Iniciación)

| Acción | Responsable | Fecha Límite | Entregable | Formato | Estado |
|--------|-------------|--------------|------------|---------|--------|
| Elaboración de Idea Canvas | Carlos Saúl Arenas Maciel | 2026-02-05 | `02_Idea_Canvas` | PDF | Pendiente |
| Reunión de Ideación | Sra. Elena Martínez + Carlos Saúl Arenas | 2026-02-07 | `03_Acta_Reunion_Ideacion` | PDF | Pendiente |
| Redacción del Project Charter (+ Matriz RACI adjunta) | Carlos Saúl Arenas Maciel | 2026-02-12 | `04_Project_Charter` + `05_Matriz_RACI` | PDF | Pendiente |
| **Revisión y Firma del Charter** | Sra. Elena Martínez (Sponsor) | 2026-02-14 | `04_Project_Charter_firmado.pdf` | PDF con firma |  **Bloqueante** |
| Reunión Go/No-Go | Steering Committee | 2026-02-17 | `06_Acta_Aprobacion_GoNoGo` | PDF con firmas |  **Bloqueante** |
| **TRANSICIÓN A FASE 1** | — | 2026-02-18 | — | — |  Desbloqueado tras firmas |


## Anexos / Fuentes Verificables

1. **INEGI (2024)**. *Censos Económicos 2024 - Resultados definitivos*. Directorio Estadístico Nacional de Unidades Económicas (DENUE): ~605,000 tiendas de abarrotes registradas en México.  
   https://www.inegi.org.mx/contenidos/saladeprensa/boletines/2025/ce/CE2024_def_RR.pdf

2. **CANACO CDMX (2025)**. *El 43% de las empresas pierde dinero por mala gestión de inventarios*. Publicación oficial en redes sociales de la Cámara Nacional de Comercio.  
   https://www.facebook.com/CANACOMexico/posts/1063578405812917

3. **INEGI (2023)**. *Estadísticas a propósito del Día de las MIPYMES*. El 98.7% de los negocios en México son micro, pequeñas y medianas empresas.  
   https://www.inegi.org.mx/contenidos/saladeprensa/aproposito/2025/EAP_MIPYMES_25.pdf