<p align="center">
  <img src="images/logo_patitas.png" alt="Logo de PATITAS" width="240">
</p>

<h1 align="center">PATITAS · Gestor de PQRS de MEPEGA</h1>

<p align="center">
  Proyecto Integrador · Algoritmia y Programación 2026-2<br>
  Facultad de Ingeniería · Departamento de Ingeniería Industrial · Universidad de Antioquia<br>
  Docente: Victor Hugo Mercado Ramos
</p>

<p align="center">
  <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" alt="Licencia CC BY-NC-SA 4.0"></a>
</p>

> **Estado actual:** versión 2.0.0 — programa completo para la Entrega 2.
> Autenticación, registro validado de PQRS, consecutivos independientes por archivo que continúan la numeración de las bases de MEPEGA, radicado de 120 columnas, consultas, cambios de estado con historial, estadísticas y exportación para Power BI.

---

## Tabla de contenido

1. [Integrantes](#1-integrantes)
2. [Vínculos académicos y descripción](#2-vínculos-académicos-y-descripción)
3. [Nombre del proyecto y detalles](#3-nombre-del-proyecto-y-detalles)
4. [Licencia del software](#4-licencia-del-software)
5. [Reporte de visión](#5-reporte-de-visión)
6. [Especificación de requisitos](#6-especificación-de-requisitos)
7. [Plan de proyecto](#7-plan-de-proyecto)
8. [Plan de versionado](#8-plan-de-versionado)
9. [Algoritmo](#9-algoritmo)
10. [Manual de usuario](#10-manual-de-usuario)
11. [GitHub](#11-github)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Cómo ejecutar el programa](#cómo-ejecutar-el-programa)
- [Actas del equipo](#actas-del-equipo)

---

## 1. Integrantes

| # | Nombre completo | Correo institucional | Rol en el proyecto |
|---|---|---|---|
| 1 | Anuar [Apellidos] | [usuario]@udea.edu.co | [Rol] |
| 2 | [Nombre y apellidos] | [usuario]@udea.edu.co | [Rol] |
| 3 | [Nombre y apellidos] | [usuario]@udea.edu.co | [Rol] |
| 4 | [Nombre y apellidos] | [usuario]@udea.edu.co | [Rol] |
| 5 | [Nombre y apellidos] | [usuario]@udea.edu.co | [Rol] |

Somos un equipo de estudiantes de pregrado de la Facultad de Ingeniería de la Universidad de Antioquia que une formación en ingeniería, análisis de datos y experiencia profesional para resolver un problema real de gestión: pasar el registro de PQRS de MEPEGA del papel a un sistema confiable, trazable y fácil de usar. Los roles se definen en el [Acta de Responsabilidad](docs/actas/03_acta_responsabilidad.md).

## 2. Vínculos académicos y descripción

### Anuar [Apellidos]
- **Programa académico:** Ingeniería Industrial — Universidad de Antioquia.
- **Habilidades:** análisis e interpretación de datos de laboratorio, control de calidad, elaboración de informes técnicos y de cumplimiento normativo, programación básica en Python.
- **Fortalezas:** rigor metodológico, orden en la documentación y experiencia profesional como químico en procesos de análisis y reporte de resultados.

### [Integrante 2]
- **Programa académico:** [Programa] — Universidad de Antioquia.
- **Habilidades:** [ej.: programación en Python, manejo de Git].
- **Fortalezas:** [ej.: liderazgo, organización, resolución de problemas].

### [Integrante 3]
- **Programa académico:** [Programa] — Universidad de Antioquia.
- **Habilidades:** [...]
- **Fortalezas:** [...]

### [Integrante 4]
- **Programa académico:** [Programa] — Universidad de Antioquia.
- **Habilidades:** [...]
- **Fortalezas:** [...]

### [Integrante 5]
- **Programa académico:** [Programa] — Universidad de Antioquia.
- **Habilidades:** [...]
- **Fortalezas:** [...]

## 3. Nombre del proyecto y detalles

<p align="center"><img src="images/logo_patitas.png" alt="Logo de PATITAS" width="180"></p>

**PATITAS** es el nuevo nombre del gestor de PQRS de MEPEGA. Evoca las huellas de los perritos y gaticos que el movimiento atiende y, al mismo tiempo, la huella que deja cada solicitud en el sistema: un número de radicado, una fecha límite y un responsable.

El logo combina tres ideas: el **globo de diálogo** representa la voz de quien presenta la petición, queja, reclamo o sugerencia; la **huella** representa a las mascotas; y el **sello de verificación** naranja representa la solicitud atendida. El verde hace referencia a la identidad de la Universidad de Antioquia.

**Descripción.** PATITAS es un programa de consola en Python que permite al equipo de MEPEGA registrar las PQRS relacionadas con la atención veterinaria de perros y gatos en los campus de la UdeA. Exige autenticación, valida cada dato al momento de digitarlo, asigna un consecutivo independiente por tipo de solicitud, guarda cada tipo en su propio archivo plano y entrega al solicitante un radicado estandarizado de 120 columnas.

**Funcionalidades de la versión 2.0.0**

| Módulo | Qué hace |
|---|---|
| Autenticación | Ingreso con usuario o correo institucional; máximo 3 intentos; bloqueo de 30 segundos con cuenta regresiva en pantalla; sesión activa visible en todas las pantallas. |
| Registro de PQRS | Captura guiada con validación de cada campo, menús numerados, opción `cancelar` y confirmación antes de guardar. |
| Almacenamiento | Cuatro archivos planos independientes con la misma estructura de 18 campos; el consecutivo continúa desde el 3001 en cada archivo. |
| Radicado | Comprobante con marco ASCII y líneas de exactamente 120 caracteres, guardado en `data/radicados/`. Ver [ejemplo](docs/ejemplo_radicado.txt). |
| Consultas | Por número de radicado (con historial de estados), por documento del solicitante, estado general, registros activos, más antiguas, próximas a vencer y vencidas. |
| Cambio de estado | Flujo obligatorio Registrada → En proceso → Solucionada, con observación, bitácora en `data/Historial.txt` y comprobante. |
| Estadísticas | Promedio de días de respuesta y cinco estadísticas adicionales en pantalla, reporte TXT y base consolidada CSV para Power BI. |

## 4. Licencia del software

Este proyecto se publica bajo la licencia **Creative Commons Atribución-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)**, seleccionada con el [selector de licencias de Creative Commons](https://chooser-beta.creativecommons.org/).

| Condición | Significado para PATITAS |
|---|---|
| **BY — Atribución** | Quien reutilice el proyecto debe dar crédito al equipo y a la Universidad de Antioquia. |
| **NC — No comercial** | No puede usarse con fines comerciales; es un desarrollo académico para una organización estudiantil. |
| **SA — Compartir igual** | Las versiones modificadas deben publicarse con esta misma licencia, para que las mejoras sigan disponibles para otros estudiantes. |

Texto completo: [LICENSE.md](LICENSE.md).

## 5. Reporte de visión

PATITAS reemplaza el registro manual en papel de las PQRS de MEPEGA por un sistema que garantiza consecutivos únicos, datos validados y trazabilidad del usuario que registra cada caso. El reporte describe el problema, los interesados, los objetivos, los beneficios, el alcance por versiones y los indicadores de éxito.

📄 [docs/01_reporte_vision.md](docs/01_reporte_vision.md)

## 6. Especificación de requisitos

Contiene 36 requisitos funcionales (35 implementados en la versión 2.0.0; el tablero de Power BI lo construye el equipo con la guía incluida) y 12 no funcionales, la tabla de reglas de validación por campo, el modelo de datos de 18 campos, la trazabilidad requisito–módulo y las preguntas abiertas para el Product Owner.

📄 [docs/02_especificacion_requisitos.md](docs/02_especificacion_requisitos.md)

## 7. Plan de proyecto

![Cronograma del proyecto](images/cronograma_gantt.png)

| Concepto | Valor |
|---|---|
| Esfuerzo total | 50 horas (25 actividades en 9 fases) |
| Valor de la hora de práctica | $8.337,64 (1 SMMLV 2026 = $1.750.905 ÷ 210 h) |
| **Presupuesto total** | **$416.882 COP** en tiempo de práctica de formación |

📄 [docs/03_plan_proyecto.md](docs/03_plan_proyecto.md) — metodología, roles, actividades, Gantt, presupuesto y riesgos.

## 8. Plan de versionado

PATITAS usa versionado semántico (`MAYOR.MENOR.PARCHE`). El plan registra 15 versiones, desde la `v0.1.0` (día 3) hasta la `v2.0.1` (día 73, sustentación), con el avance acumulado de cada una medido sobre las 50 horas del plan de proyecto.

![Avance por versión](images/avance_versiones.png)

📄 [docs/04_plan_versionado.md](docs/04_plan_versionado.md)

## 9. Algoritmo

Todo el código está en la carpeta [`src/`](src): 11 módulos en Python que usan solo la biblioteca estándar.

| Módulo | Responsabilidad |
|---|---|
| `main.py` | Punto de entrada, menú principal y menú de estadísticas |
| `config.py` | Rutas, catálogos y reglas de negocio |
| `interfaz.py` | Banner, pantallas, tablas paginadas y lectura de la clave |
| `autenticacion.py` | Ingreso, intentos, bloqueo y sesión |
| `validaciones.py` | Reglas de validación de cada campo y del flujo de estados |
| `registro.py` | Registrar PQRS |
| `consultas.py` | Consultar PQRS |
| `cambios.py` | Registrar cambio de estado |
| `reportes.py` | Estadísticas y exportación para Power BI |
| `archivos.py` | Lectura y escritura de los archivos planos |
| `radicado.py` | Comprobante de 120 columnas |

📄 [docs/05_algoritmo.md](docs/05_algoritmo.md) — arquitectura, estructuras de datos, diagramas de flujo, pseudocódigo, pruebas y preguntas de repaso para la sustentación.

## 10. Manual de usuario

Guía paso a paso con capturas de pantalla: instalación, ingreso, registro, consultas, cambios de estado, estadísticas, archivos generados, configuración y solución de problemas.

📄 [docs/06_manual_usuario.md](docs/06_manual_usuario.md)

## 11. GitHub

Repositorio creado por el líder con su cuenta institucional de la UdeA y compartido con todos los integrantes como colaboradores.

| Carpeta | Contenido |
|---|---|
| `src/` | Código fuente Python |
| `docs/` | Documentación, manual de usuario y actas |
| `images/` | Logo, diagramas y capturas del manual |
| `data/` | `Peticion.txt`, `Queja.txt`, `Reclamo.txt`, `Sugerencia.txt`, usuarios, historial y archivos generados |

📄 [docs/07_guia_github.md](docs/07_guia_github.md) — creación de la cuenta, carga del proyecto, vinculación de compañeros, trabajo con ramas, versiones y lista de verificación.

---

## Estructura del repositorio

```
/
├── README.md
├── LICENSE.md
├── src/                          # Código fuente Python
│   ├── main.py                   # Punto de entrada y menú principal
│   ├── config.py                 # Rutas, catálogos y reglas de negocio
│   ├── interfaz.py               # Banner, pantallas, tablas y lectura de la clave
│   ├── autenticacion.py          # Login, intentos, bloqueo y sesión
│   ├── validaciones.py           # Reglas de validación y flujo de estados
│   ├── registro.py               # Opción 1: registrar PQRS
│   ├── consultas.py              # Opción 2: consultar PQRS
│   ├── cambios.py                # Opción 3: cambio de estado
│   ├── reportes.py               # Opción 4: estadísticas y Power BI
│   ├── archivos.py               # Lectura/escritura de los archivos planos
│   └── radicado.py               # Comprobante de 120 columnas
├── docs/                         # Documentación
│   ├── 01_reporte_vision.md
│   ├── 02_especificacion_requisitos.md
│   ├── 03_plan_proyecto.md
│   ├── 04_plan_versionado.md
│   ├── 05_algoritmo.md
│   ├── 06_manual_usuario.md
│   ├── 07_guia_github.md
│   ├── 08_guia_power_bi.md
│   ├── ejemplo_radicado.txt
│   └── actas/                    # Actas del equipo
├── images/                       # Logo, diagramas y capturas del manual
└── data/                         # Archivos planos del programa
    ├── Peticion.txt
    ├── Queja.txt
    ├── Reclamo.txt
    ├── Sugerencia.txt
    ├── Usuarios.txt
    ├── Historial.txt             # Bitácora de cambios de estado
    ├── radicados/                # Radicados y comprobantes generados
    └── exportaciones/            # Reportes TXT y base CSV para Power BI
```

## Cómo ejecutar el programa

**Requisitos:** Python 3.10 o superior. No se necesitan librerías externas.

```bash
git clone https://github.com/[usuario-lider]/[nombre-repositorio].git
cd [nombre-repositorio]
python src/main.py
```

- Ingrese con cualquier usuario activo de `data/Usuarios.txt`, ya sea con el nombre de usuario (por ejemplo, `admin_udea`) o con el correo institucional.
- Para ejecutar las pruebas de las reglas de validación y del flujo de estados: `python src/validaciones.py`
- Instrucciones completas en el [manual de usuario](docs/06_manual_usuario.md).
- Si la consola de su editor no muestra los asteriscos al escribir la clave, cambie `MOSTRAR_ASTERISCOS = False` en `src/config.py`.

## Actas del equipo

| Acta | Archivo |
|---|---|
| Acta de Entendimiento | [docs/actas/01_acta_entendimiento.md](docs/actas/01_acta_entendimiento.md) |
| Acta de Colaboración | [docs/actas/02_acta_colaboracion.md](docs/actas/02_acta_colaboracion.md) |
| Acta de Responsabilidad | [docs/actas/03_acta_responsabilidad.md](docs/actas/03_acta_responsabilidad.md) |
| Plantilla de acta de seguimiento | [docs/actas/04_plantilla_acta_seguimiento.md](docs/actas/04_plantilla_acta_seguimiento.md) |

---

<sub>El nombre "MEPEGA" (Movimiento Estudiantil de Perritos y Gaticos) es una denominación ficticia de carácter humorístico utilizada con fines académicos, según el enunciado del curso.</sub>
