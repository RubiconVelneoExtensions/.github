# Rubicon Velneo Extensions 🚀

> Suite oficial de herramientas de ingeniería, desarrollo asistido por IA y automatización para el ecosistema **Velneo vDevelop** y **vClient Runtime**.  
> Desarrollado e impulsado por el equipo técnico de **[Rubicon Consultoría y Desarrollo de Software SLU](https://www.rubiconsulting.es/)**.

---

## 🏢 Sobre Rubicon Software

En **Rubicon**, como Partner Oficial de Velneo líder en España, desarrollamos soluciones tecnológicas avanzadas para optimizar el ciclo de desarrollo, la calidad del código y la integración de inteligencia artificial en aplicaciones empresariales Velneo.

> 🔒 **Acceso Interno**: Los repositorios, motores y paquetes de esta suite son de uso interno y privado. Los miembros autorizados del equipo de desarrollo y consultoría de Rubicon pueden acceder a la documentación técnica, descargas y guías en el repositorio privado [**.github-private**](https://github.com/RubiconVelneoExtensions/.github-private).

---

## 🛠️ Tecnologías y Compatibilidad

![Velneo](https://img.shields.io/badge/Velneo-v35%20--%20v37-0052cc?style=for-the-badge&logo=cplusplus&logoColor=white)
![MCP Protocol](https://img.shields.io/badge/Model%20Context%20Protocol-MCP%20v1.0-8a2be2?style=for-the-badge&logo=anthropic&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.10%20%7C%203.11%20%7C%203.14-3776ab?style=for-the-badge&logo=python&logoColor=white)
![Qt / QML](https://img.shields.io/badge/Qt%20%2F%20QML-5.15%20QtQuick-41cd52?style=for-the-badge&logo=qt&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES5%20%2F%20V8-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)
![Windows](https://img.shields.io/badge/OS-Windows%2010%20%7C%2011%20%28x64%29-0078d6?style=for-the-badge&logo=windows&logoColor=white)

---

## 🗺️ Arquitectura de la Suite

La suite conecta los entornos modernos de desarrollo asistido por IA (LLMs) con la memoria viva de Velneo vDevelop y el runtime de datos de vClient:

```mermaid
flowchart TD
    subgraph IA ["🤖 Modelos de Lenguaje & Entornos de IA"]
        LLM["Antigravity / Claude / Copilot"]
    end

    subgraph Hub ["🌉 Puente Central MCP (127.0.0.1:21845)"]
        MCP["Puente Guía Hub (server.js)<br/>stdio + HTTP JSON-RPC"]
    end

    subgraph Extensions ["🧩 Suite de Extensiones vDevelop"]
        PG["Puente Guía<br/>(McpBridge & Asistente)"]
        CS["Code Sync 2D<br/>(Sincronizador Incremental)"]
        CI["Code IDE<br/>(Visor & Auditor AST)"]
        VI["Variables IDE<br/>(Gestión UIA)"]
        BO["Buscador Objetos<br/>(Índice en Memoria)"]
    end

    subgraph Velneo ["🏢 Entorno de Desarrollo y Runtime Velneo"]
        VD["Velneo vDevelop<br/>(Diseño, Procesos, MTI)"]
        VC["Velneo vClient<br/>(Runtime de Datos en Vivo)"]
    end

    LLM <-->|Herramientas MCP| MCP
    MCP <-->|REST / Polling 1s| PG
    PG <-->|RAM theExtension / theApp| VD
    CS <-->|Inyección UIA & JSON| VD
    CI <-->|Inspección y AST| VD
    VI <-->|UIA Automatización| VD
    BO <-->|Caché de Búsqueda| VD
    MCP -.->|Auditoría / Conexión| VC
```

---

## 🧩 Herramientas del Ecosistema

- **Puente Guía**: Servidor MCP híbrido (stdio/HTTP) para inspección en memoria viva, navegación interactiva y asistencia por IA en vDevelop.
- **vDevelop Code Sync (1D & 2D)**: Sincronización continua de procesos y código fuente en escritorios secundarios aislados.
- **vDevelop Code IDE**: Visor de código con análisis sintáctico AST, linter y auditoría de calidad.
- **vDevelop Variables IDE**: Automatización UIA para la creación, reordenación y tipado masivo de variables locales.
- **vDevelop Buscador de Objetos**: Búsqueda global instantánea indexada en memoria viva por tipo, ID y nombre.
- **Velneo Skills**: Catálogo maestro de sintaxis, reglas canónicas y contexto especializado para modelos de lenguaje.

---

## 📬 Contacto y Colaboración

Para consultas sobre nuestras soluciones, consultoría especializada o servicios de desarrollo empresarial con Velneo:

- 🌐 **Sitio Web Oficial**: [rubiconsulting.es](https://www.rubiconsulting.es/)
- ✉️ **Contacto**: [rubiconsulting.es/es/contacto](https://www.rubiconsulting.es/es/contacto)
- 💼 **LinkedIn**: [Rubicon Consultoría y Desarrollo de Software](https://www.linkedin.com/company/rubicon-software)
