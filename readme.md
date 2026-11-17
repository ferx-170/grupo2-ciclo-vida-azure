# Ciclo de Vida de Datos en la Nube: Optimización de Costos de Registros de Auditoría

**Trabajo de Investigación Aplicada — Grupo N.° 2**

## Descripción del Proyecto
Este repositorio contiene los recursos técnicos y la documentación de la práctica sobre gestión del ciclo de vida de datos (ILM/DLM) en almacenamiento en la nube. El proyecto demuestra cómo optimizar los costos de almacenamiento clasificando archivos según su frecuencia de acceso mediante los niveles **Hot**, **Cool** y **Archive**, y automatizando su transición y expiración.

## Caso Práctico: Registros de Auditoría (Opción B)
* **Escenario:** Sistema integrado de gestión municipal (*Municipalidad Modelo* — datos 100 % ficticios).
* **Patrón de uso:** Los registros de acceso (*logs*) y reportes diarios se revisan activamente durante los primeros días para detectar fallas o incidentes de seguridad, luego se consultan rara vez y finalmente se conservan por respaldo administrativo antes de su eliminación definitiva.

## Política de Ciclo de Vida Aplicada

| Días desde la creación | Acción | Nivel de almacenamiento | Propósito operativo |
| :--- | :--- | :--- | :--- |
| **0 – 30 días** | Carga inicial | **Hot** | Consulta inmediata y monitoreo diario |
| **Día 30** | Transición | **Cool** | Almacenamiento de acceso poco frecuente |
| **Día 90** | Transición | **Archive** | Resguardo económico para auditorías e investigaciones |
| **Día 365** | Expiración | **Eliminación** | Cumplimiento de retención y limpieza automática |

## Estructura del Repositorio

```text
├── reglas/              # Código exportado (JSON / XML) de la regla de ciclo de vida
├── datos-prueba/        # Archivos ficticios usados en la práctica (auditoria-2026/ y logs/)
└── README.md            # Información general del proyecto y del equipo
```

## Equipo — Grupo N.° 2
* **Institución / Programa:** [Completar nombre de la institución y carrera]
* **Asignatura:** [Completar nombre del curso]
* **Docente:** [Completar nombre del docente]
* **Proveedor Cloud utilizado:** [AWS S3 / Google Cloud Storage / Azure Blob Storage]

### Integrantes
1. [Apellidos y Nombres — Integrante 1]
2. [Apellidos y Nombres — Integrante 2]
3. [Apellidos y Nombres — Integrante 3]
4. [Apellidos y Nombres — Integrante 4]

---
> **Nota de seguridad:** Todos los archivos de prueba contenidos en este repositorio utilizan datos ficticios. No se incluyen credenciales, llaves de acceso ni identificadores sensibles de cuentas en la nube.