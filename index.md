import os
from weasyprint import HTML

# Content for the Enhanced Markdown File (v2)
markdown_v2 = """# 🚀 El Futuro del Código: Creative Programming 2024

![Versión](https://img.shields.io/badge/version-2.0-blue?style=for-the-badge)
![Estatus](https://img.shields.io/badge/status-active-success?style=for-the-badge)
![Tecnologías](https://img.shields.io/badge/tech-HTML|CSS|JS|Python-orange?style=for-the-badge)

---

## 📑 Menú de Navegación
[🏠 Inicio](#) | [💡 Proyectos](#proyectos) | [🤖 IA & Futuro](#ia) | [🛠️ Recursos](#recursos) | [📫 Contacto](#)

---

## 💡 Galería de Proyectos Innovadores

> "La programación no es sobre lo que sabes, es sobre lo que puedes imaginar."

### 🟢 Nivel: Explorador
**Proyecto: El Pintor Algorítmico**
* **Descripción:** Una web que genera patrones artísticos basados en la frecuencia de tu voz.
* **Stack:** `JavaScript` + `Web Audio API`.
* **Impacto:** Arte digital único y accesible.

### 🟡 Nivel: Arquitecto
**Proyecto: Eco-Monitor de Código**
* **Descripción:** Una extensión de VS Code que calcula cuántos gramos de CO2 genera la ejecución de tu script.
* **Stack:** `Python` + `Rust` + `VS Code API`.
* **Impacto:** Conciencia sobre la sostenibilidad digital.

### 🔴 Nivel: Maestro
**Proyecto: Simulación de Colmena IA**
* **Descripción:** Cientos de agentes inteligentes que colaboran para resolver un laberinto en 3D.
* **Stack:** `TensorFlow.js` + `Three.js`.
* **Impacto:** Investigación en inteligencia colectiva.

---

## 🤖 El Impacto de la Inteligencia Artificial

La IA no es el fin del programador, es su **exosqueleto**.

| Habilidad | Rol de la IA | Valor Humano |
| :--- | :--- | :--- |
| **Escritura** | Autocompletado de sintaxis | Arquitectura del sistema |
| **Depuración** | Identificación de patrones de error | Toma de decisiones crítica |
| **Seguridad** | Análisis de vulnerabilidades | Ética y privacidad |

---

## 🛠️ Caja de Herramientas del Programador Moderno

### 📚 Aprendizaje
* [**roadmap.sh**](https://roadmap.sh) - Guías visuales para cada carrera tecnológica.
* [**FreeCodeCamp**](https://freecodecamp.org) - Práctica real con certificación.

### ⚡ Productividad
* [**Raycast**](https://raycast.com) - El lanzador definitivo para macOS.
* [**Oh My Zsh**](https://ohmyz.sh) - Mejora tu terminal al máximo.

---

## 🌍 Únete a la Conversación
¿Tienes una idea loca? No la guardes. El código es el lenguaje que construye el mañana.

---
*Hecho con ❤️ para mentes curiosas por el desarrollo.*
"""

# HTML for the PDF Preview (making it look like a "Beautiful Page")
html_content = f"""
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <style>
        @page {{
            size: A4;
            margin: 0;
            background-color: #0f172a;
        }}
        body {{
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            color: #f8fafc;
            margin: 0;
            padding: 40px;
            background-color: #0f172a;
            line-height: 1.6;
        }}
        .container {{
            max-width: 800px;
            margin: 0 auto;
        }}
        header {{
            border-bottom: 2px solid #334155;
            padding-bottom: 20px;
            margin-bottom: 30px;
            text-align: center;
        }}
        h1 {{
            color: #38bdf8;
            font-size: 28pt;
            margin-bottom: 10pt;
        }}
        .nav {{
            color: #94a3b8;
            font-size: 10pt;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 30px;
        }}
        h2 {{
            color: #7dd3fc;
            border-left: 5px solid #0ea5e9;
            padding-left: 15px;
            margin-top: 40px;
            font-size: 18pt;
        }}
        .card {{
            background: #1e293b;
            border: 1px solid #334155;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
        }}
        .card h3 {{
            color: #f472b6;
            margin-top: 0;
        }}
        .badge {{
            display: inline-block;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 9pt;
            font-weight: bold;
            margin-bottom: 10px;
        }}
        .badge-blue {{ background: #1d4ed8; color: white; }}
        .badge-green {{ background: #15803d; color: white; }}
        
        table {{
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            background: #1e293b;
            border-radius: 8px;
            overflow: hidden;
        }}
        th, td {{
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #334155;
        }}
        th {{
            background: #334155;
            color: #38bdf8;
        }}
        blockquote {{
            font-style: italic;
            color: #94a3b8;
            border-left: 4px solid #334155;
            padding-left: 20px;
            margin: 20px 0;
        }}
        footer {{
            margin-top: 50px;
            text-align: center;
            font-size: 9pt;
            color: #64748b;
        }}
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="nav">🏠 Inicio | 💡 Proyectos | 🤖 IA | 🛠️ Recursos</div>
            <h1>El Futuro del Código</h1>
            <p>Explorando la frontera del desarrollo de software y la creatividad.</p>
        </header>

        <blockquote>"La programación no es sobre lo que sabes, es sobre lo que puedes imaginar."</blockquote>

        <h2>💡 Ideas de Proyectos</h2>
        
        <div class="card">
            <span class="badge badge-blue">JS + Canvas</span>
            <h3>El Pintor Algorítmico</h3>
            <p>Generación de arte generativo mediante frecuencias de sonido capturadas en el navegador.</p>
        </div>

        <div class="card">
            <span class="badge badge-green">Python + Rust</span>
            <h3>Eco-Monitor de Código</h3>
            <p>Herramienta para medir la huella de carbono de algoritmos en tiempo real.</p>
        </div>

        <h2>🤖 La Era de la IA</h2>
        <table>
            <thead>
                <tr>
                    <th>Habilidad</th>
                    <th>Rol de la IA</th>
                    <th>Valor Humano</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Escritura</td>
                    <td>Autocompletado</td>
                    <td>Arquitectura</td>
                </tr>
                <tr>
                    <td>Depuración</td>
                    <td>Análisis de patrones</td>
                    <td>Decisión crítica</td>
                </tr>
            </tbody>
        </table>

        <footer>
            Desarrollado para la comunidad de programadores curiosos • 2024
        </footer>
    </div>
</body>
</html>
"""

# Save Markdown File
md_path = "web_programacion_v2.md"
with open(md_path, "w", encoding="utf-8") as f:
    f.write(markdown_v2)

# Save PDF Preview
pdf_path = "preview_pagina_programacion.pdf"
temp_html = "temp_preview.html"
with open(temp_html, "w", encoding="utf-8") as f:
    f.write(html_content)

HTML(filename=temp_html).write_pdf(pdf_path)
os.remove(temp_html)

print(f"Files saved: {md_path} and {pdf_path}")
