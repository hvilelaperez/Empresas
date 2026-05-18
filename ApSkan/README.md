## 🧰 Tecnologías Aplicadas en APSKAN


### Frontend
| Tecnología | Uso en tus proyectos |
|------------|----------------------|
| **Next.js 16** | Framework full-stack (App Router) para OrAiFlow2 y DentalSkan |
| **React 19** | Libreria core para interfaces de usuario |
| **TypeScript 5** | Tipado estricto (modo strict) en ambos proyectos |
| **Tailwind CSS** | Estilizado rápido y consistente |
| **shadcn/ui** | Componentes accesibles (basados en Radix UI) |
| **Zustand** | Estado global (ligero, poco boilerplate) |
| **TanStack Query** | Data fetching, caché y sincronización |
| **D3.js + DC.js** | Gráficos interactivos con filtros cruzados (Crossfilter) |

### Backend & API
| Tecnología | Uso en tus proyectos |
|------------|----------------------|
| **Node.js** | API Routes en Next.js |
| **Prisma** | ORM (schema definido para PostgreSQL, pendiente conexión) |
| **PostgreSQL** | Base de datos relacional (en roadmap) |
| **SQLite** | Base de datos ligera para Engram (memoria persistente) |
| **Clerk** | Autenticación (SDK v6, roles: admin, odontólogo, recepcionista) |

### IA y Orquestación
| Tecnología | Uso en tus proyectos |
|------------|----------------------|
| **OpenRouter** | Agregador de múltiples proveedores IA |
| **NVIDIA API** | Proveedor alternativo de modelos |
| **DeepSeek** | Proveedor alternativo de modelos |
| **Engram** | Memoria persistente para IA (SQLite backend) |
| **NotebookLM** | Ingeniería de contexto y grounding |
| **MCP (Model Context Protocol)** | Conexión con Jira, Notion, bases de datos |

### DevOps & Herramientas
| Tecnología | Uso en tus proyectos |
|------------|----------------------|
| **GitHub Actions** | Automatización CI/CD, revisiones automáticas en PR |
| **Git Worktrees** | Trabajo paralelo con subagentes sin colisiones |
| **File System (fs)** | Guardado local en `InOuFiles` (privacidad, control total) |

### Metodologías y Estándares
| Metodología/Estándar | Aplicación |
|----------------------|-------------|
| **SDD (Spec-Driven Development)** | Generación de documentación ERS v4.0 desde especificación |
| **OWASP** | Seguridad por diseño, auditoría de código generado por IA |
| **Ingeniería de Contexto** | `agents.md` / `claud.md` como fuente de verdad |
| **Arquitectura Distribuida / Microservicios** | Diseño asistido por IA |

---

## 🏗️ Sistemas Desarrollados en APSKAN

### 1. OrAiFlow2 – Generador de Documentación Técnica ERS v4.0 con IA

**Propósito:** Automatizar la generación de especificaciones técnicas siguiendo SDD.

**Módulos clave:**
- Panel de Configuración API (multi-proveedor)
- Generación de Fuente de Verdad (FdV)
- Generación de ERS v4.0 (10 dimensiones)
- Editor de Perfil (persistente en `00_Perfil.md`)
- Integración Engram (memoria persistente)
- Guardado local en `InOuFiles`
- Validaciones (protección de archivos base)

**Impacto:** 95% reducción en tiempo de generación, cero inconsistencias.

---

### 2. DentalSkan – Sistema de Gestión Clínica Dental

**Propósito:** Optimizar operación de clínicas dentales (historias clínicas digitales, citas, odontograma, periodontograma, planes de tratamiento versionados, reportes analíticos).

**Módulos y estado:**
| Módulo | Estado | Complejidad |
|--------|--------|-------------|
| Pacientes + Odontograma (32 piezas + temporales) | ✅ 90% | Muy Alta |
| Periodontograma (sondaje, sangrado, movilidad) | ✅ Completado | Alta |
| Planes de tratamiento versionados (previo→previsto→realizado) | ✅ Completado | Muy Alta |
| Agenda (día/semana/mes) | ✅ 80% | Media |
| Reportes con DC.js + Crossfilter | ✅ Completado | Alta |
| Usuarios Clínicos (Wizard 3 pasos) | ✅ Completado | Media-Alta |
| Autenticación (Clerk, roles) | ✅ Completado | Media |
| CMR (Clientes potenciales) | 🔄 En desarrollo | Media |
| Treatments (catálogo) | ⏳ Por iniciar | Baja |

**Pendiente:** Conexión con Prisma + PostgreSQL (schema definido, actualmente localStorage).

---