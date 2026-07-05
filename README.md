# Guía de Estructura de Noticias — PternaSec/news

Este repositorio actúa como el feed de novedades, boletines técnicos de ciberseguridad, análisis de vulnerabilidades y actualizaciones de la plataforma.

## Estructura de Directorios

Cada noticia se define en una subcarpeta dedicada con su archivo de metadatos `README.md`.

```
news/
├── java-serialization-rce/ ← Slug único de la noticia (slug en minúsculas)
│   └── README.md           ← OBLIGATORIO (con Frontmatter YAML)
└── waf-bypass-release/
    └── README.md
```

---

## Formato del README.md (Frontmatter YAML)

Cada noticia debe contener un `README.md` con un bloque superior Frontmatter YAML delimitado por `---` para definir las propiedades:

```markdown
---
title: "Nueva vulnerabilidad crítica Zero-Day en librerías de serialización de Java"
category: alerta
date: "2026-07-05T00:00:00Z"
read_time: "4 min"
cve: "CVE-2026-4402"
severity: critical
description: "Se ha publicado una vulnerabilidad que permite la ejecución remota de código en varios frameworks."
---

## Análisis Técnico

Aquí va el contenido largo de la noticia o boletín de seguridad en formato Markdown estándar...
```

---

## Opciones Disponibles para los Campos

### 1. Categorías de Boletín (`category`)
Determina el tipo de publicación y la etiqueta correspondiente en la interfaz del dashboard. Opciones admitidas:
- `alerta` (Alerta de seguridad - Color Rojo)
- `tutorial` (Guía o Tutorial práctico - Color Esmeralda)
- `actualizacion` (Actualización de plataforma o del sistema - Color Azul)
- `analisis` (Análisis técnico de exploits o malware - Color Púrpura)

### 2. Fecha (`date`)
La fecha debe estar en formato **ISO 8601** (ej. `"2026-07-05T00:00:00Z"`). 
El dashboard utiliza esta fecha para ordenar las noticias (de más reciente a más antigua) y para mostrar dinámicamente textos como:
- *"Hace 2 horas"*
- *"Ayer"*
- *"Hace 3 días"*

### 3. Tiempo de lectura (`read_time`)
Es el string que define el tiempo promedio estimado para leer la noticia (ej. `"4 min"`, `"12 min"`).

### 4. Gravedad de la Noticia (`severity` - Opcional)
Se puede definir para alertas de vulnerabilidad que tengan un nivel de riesgo asociado. Opciones admitidas:
- `critical` (Crítica)
- `high` (Alta)
- `medium` (Media)
- `low` (Baja)

### 5. Identificador CVE (`cve` - Opcional)
Identificador oficial de la vulnerabilidad en la base de datos de MITRE si aplica (ej. `"CVE-2026-4402"`). La UI mostrará una pequeña insignia con este código al lado del título.
