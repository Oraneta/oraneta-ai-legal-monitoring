
<div align="center">

# ORANETA AI
## Monitoreo Jurídico Inteligente

### Inteligencia artificial y automatización del Diario Oficial de la Federación

**Una solución desarrollada por Oraneta para Inteligencia Jurídica que transforma publicaciones oficiales en información útil, alertas personalizadas y servicios automatizados a través de WhatsApp.**

<img src="https://img.shields.io/badge/Inteligencia_Artificial-168BFF?style=for-the-badge" alt="Inteligencia Artificial">
<img src="https://img.shields.io/badge/RAG-643BFF?style=for-the-badge" alt="RAG">
<img src="https://img.shields.io/badge/WhatsApp-C329F4?style=for-the-badge" alt="WhatsApp">

<br><br>

**Proyecto desarrollado por [Oraneta](https://oraneta.com) para [Inteligencia Jurídica](https://inteligenciajuridica.mx)**

</div>

---

## Acerca del proyecto

**Oraneta AI | Monitoreo Jurídico Inteligente** es una aplicación empresarial que combina inteligencia artificial, procesamiento documental, búsqueda semántica y automatización de procesos para facilitar el acceso a la información publicada en el Diario Oficial de la Federación (DOF) de México.

Desarrollada por **Oraneta para Inteligencia Jurídica**, la solución permite monitorear publicaciones oficiales, identificar información relevante para cada usuario, generar alertas personalizadas y responder consultas jurídicas mediante WhatsApp.

Además, incorpora funcionalidades comerciales y administrativas para gestionar suscripciones, renovaciones, pagos, facturación y atención al cliente desde una misma experiencia conversacional.

El proyecto demuestra cómo la inteligencia artificial puede integrarse con sistemas empresariales para automatizar procesos completos, más allá de responder preguntas.

---

## ¿Qué problema resuelve?

El Diario Oficial de la Federación publica diariamente disposiciones jurídicas, acuerdos, decretos, resoluciones y otros documentos oficiales que pueden afectar a empresas, profesionales y ciudadanos.

Identificar oportunamente la información relevante requiere revisar publicaciones extensas, interpretar su contenido y dar seguimiento a temas específicos.

**Oraneta AI automatiza este proceso para:**

- Detectar nuevas publicaciones del DOF.
- Procesar y organizar información jurídica.
- Identificar publicaciones relacionadas con los intereses de cada usuario.
- Generar alertas personalizadas.
- Facilitar consultas mediante lenguaje natural.
- Reducir el trabajo manual de seguimiento documental.
- Automatizar la contratación y administración del servicio.

---

## Funcionalidades principales

### Monitoreo automatizado del DOF

La aplicación consulta periódicamente el Diario Oficial de la Federación para detectar nuevas publicaciones.

Procesa documentos PDF, extrae su contenido y organiza la información para su posterior consulta y análisis.

El sistema contempla las ediciones matutinas y vespertinas y mecanismos para identificar nuevas publicaciones.

### Alertas jurídicas inteligentes

Los usuarios pueden definir temas de interés para recibir información relacionada con sus necesidades.

La aplicación analiza las publicaciones y determina su relevancia mediante inteligencia artificial.

Las alertas pueden incluir resúmenes y referencias que facilitan localizar la información dentro de la publicación oficial.

### Consultas jurídicas con inteligencia artificial

Permite realizar preguntas en lenguaje natural sobre la información procesada del DOF.

Combina recuperación de información y generación de respuestas mediante modelos de OpenAI.

El sistema utiliza búsquedas semánticas y textuales para recuperar contenido relevante y construir respuestas fundamentadas en las publicaciones disponibles.

### Asistente conversacional por WhatsApp

WhatsApp funciona como el principal canal de interacción con los usuarios.

El asistente interpreta las solicitudes y las dirige automáticamente a módulos especializados.

Puede atender consultas, proporcionar información, gestionar servicios y acompañar al usuario durante distintos procesos.

### Gestión de suscripciones

Automatiza la incorporación de nuevos clientes y la contratación del servicio.

Incluye mecanismos para gestionar pruebas gratuitas, planes comerciales, promociones y registro de usuarios.

### Pagos y renovaciones

Integra Mercado Pago para facilitar la contratación y renovación de suscripciones.

El asistente puede acompañar al usuario durante el proceso de pago y gestionar información relacionada con la vigencia de su servicio.

### Facturación electrónica

Incorpora un módulo de facturación conectado con un servicio especializado.

Permite gestionar datos fiscales, solicitudes de facturación y operaciones relacionadas con comprobantes fiscales digitales.

### Administración de alertas y preferencias

Los usuarios pueden administrar sus intereses de seguimiento mediante conversaciones con el asistente.

Entre las operaciones disponibles se encuentran:

- Crear, modificar y eliminar alertas.
- Administrar preferencias de recordatorios.
- Configurar preferencias promocionales.
- Consultar información sobre la vigencia del servicio.

### Memoria conversacional

La aplicación conserva el historial de las conversaciones en PostgreSQL.

Esto permite mantener el contexto entre mensajes y ofrecer continuidad en la atención.

### Atención y escalamiento humano

Cuando una solicitud requiere intervención especializada, el sistema puede registrar el caso y notificar a un administrador.

Este mecanismo permite combinar automatización con atención humana.

### Seguimiento y análisis operativo

Registra eventos relacionados con el uso de la aplicación, adquisición de usuarios, cambios de alertas y resultados del procesamiento.

Esta información facilita el seguimiento de la operación y el análisis del servicio.

---

## Arquitectura tecnológica

La aplicación utiliza una arquitectura modular que combina inteligencia artificial, servicios externos, automatización y almacenamiento persistente.

| Componente | Tecnología |
|---|---|
| Lenguaje principal | Python |
| Backend y servicios HTTP | FastAPI |
| Inteligencia artificial | OpenAI API |
| Modelos de lenguaje | GPT, configurable |
| Arquitectura de recuperación | RAG |
| Búsqueda semántica | OpenAI Embeddings |
| Base de datos | PostgreSQL |
| Búsqueda vectorial | pgvector / HNSW |
| Procesamiento documental | PyPDF |
| Canal conversacional | Meta WhatsApp Cloud API |
| Integración de pagos | Mercado Pago |
| Facturación electrónica | API externa de facturación |
| Validación de datos | Pydantic |
| Comunicación entre servicios | API REST y webhooks |

### Flujo de funcionamiento

```text
Diario Oficial de la Federación
              |
              v
Monitoreo automatizado
              |
              v
Descarga y procesamiento de PDF
              |
              v
Extracción y organización del contenido
              |
              v
Generación de embeddings
              |
              v
PostgreSQL + búsqueda vectorial
              |
              v
Análisis de relevancia con IA
              |
              v
Alertas jurídicas personalizadas
              |
              v
WhatsApp Business
              |
              v
Usuario final
```

### Flujo del asistente conversacional

```text
Usuario de WhatsApp
          |
          v
Meta WhatsApp Cloud API
          |
          v
Webhook / FastAPI
          |
          v
Oraneta AI
Clasificación de intenciones
          |
          v
Enrutamiento inteligente
          |
          +-- Información general
          |
          +-- Consultas jurídicas
          |
          +-- Suscripciones
          |
          +-- Renovaciones
          |
          +-- Administración
          |
          +-- Facturación
          |
          +-- Ayuda
          |
          v
Ejecución del módulo correspondiente
          |
          v
PostgreSQL / OpenAI / Servicios externos
          |
          v
Respuesta por WhatsApp
```

---

## Prueba la aplicación

La solución está diseñada para interactuar con los usuarios a través de WhatsApp.

La demostración permite conocer cómo funciona un asistente empresarial capaz de combinar información jurídica, inteligencia artificial y automatización operativa.

### Acceso a la demostración

**El enlace de acceso a la demostración se incorporará próximamente.**

### ¿Qué puedes probar?

**1. Conversación con inteligencia artificial**

Inicia una conversación con el asistente y solicita información sobre el servicio de monitoreo jurídico.

**2. Consultas sobre el DOF**

Realiza preguntas relacionadas con las publicaciones oficiales disponibles.

Ejemplos:

- ¿Qué se publicó hoy en el Diario Oficial de la Federación?
- ¿Hay publicaciones relacionadas con comercio exterior?
- ¿Qué información existe sobre disposiciones fiscales?
- ¿Puedes resumir una publicación del DOF?

**3. Alertas personalizadas**

Consulta cómo funcionan las alertas jurídicas y solicita información sobre la configuración de temas de interés.

**4. Administración del servicio**

Explora las opciones disponibles para gestionar preferencias, consultar suscripciones y recibir asistencia.

**5. Procesos comerciales**

Conoce cómo el asistente acompaña a los usuarios durante la contratación, renovación y administración de sus servicios.

### Consideraciones

- La demostración requiere conexión a Internet.
- Las funcionalidades disponibles pueden depender del estado de la suscripción.
- Las respuestas jurídicas se generan a partir de la información documental disponible.
- Las operaciones comerciales pueden requerir datos adicionales y confirmaciones.
- No es necesario instalar software para interactuar mediante WhatsApp.
- La disponibilidad del acceso público está sujeta a la habilitación de la demostración.

---

## Aplicaciones empresariales

Aunque esta implementación está especializada en información jurídica mexicana, la arquitectura de Oraneta AI puede adaptarse a diferentes sectores y procesos empresariales.

### Monitoreo regulatorio

Seguimiento de disposiciones, publicaciones y cambios normativos relevantes para una organización.

### Gestión documental inteligente

Procesamiento y consulta de documentos mediante inteligencia artificial y recuperación semántica.

### Atención automatizada al cliente

Asistentes que resuelven consultas y ejecutan procesos operativos a través de canales conversacionales.

### Automatización comercial

Gestión de clientes, suscripciones, pagos, renovaciones y procesos administrativos.

### Servicios de información especializados

Plataformas que transforman grandes volúmenes de información en respuestas y alertas personalizadas.

---

## Modelo de implementación

Este proyecto representa una implementación de Oraneta AI desarrollada para las necesidades de Inteligencia Jurídica.

La solución combina componentes reutilizables de inteligencia artificial y automatización con procesos especializados del sector jurídico.

Su arquitectura modular permite adaptar los asistentes, las fuentes de información, las reglas de negocio y las integraciones a distintos entornos empresariales.

Cada implementación puede requerir configuraciones, integraciones y controles específicos según las necesidades del cliente.

---

## Sobre el código fuente

Este repositorio tiene fines exclusivamente de documentación, presentación tecnológica y portafolio profesional.

**El código fuente de Oraneta AI es privado y no se distribuye públicamente.**

El repositorio presenta las capacidades funcionales, la arquitectura general y el caso de implementación desarrollado para Inteligencia Jurídica.

La publicación de esta documentación no concede licencias de uso, reproducción, modificación o distribución del software propietario.

---

## Acerca de Inteligencia Jurídica

**[Inteligencia Jurídica](https://inteligenciajuridica.mx)** es una plataforma especializada en información y conocimiento legal mexicano.

Combina herramientas tecnológicas con contenido jurídico estructurado para facilitar el acceso a legislación, jurisprudencia, conceptos jurídicos y recursos especializados.

La implementación de Oraneta AI amplía estas capacidades mediante monitoreo automatizado del DOF, alertas personalizadas y atención conversacional inteligente.

---

## Acerca de Oraneta

**[Oraneta](https://oraneta.com)** desarrolla plataformas de asistentes digitales empresariales que combinan inteligencia artificial, automatización de procesos e integración con sistemas corporativos.

Sus soluciones permiten interactuar con clientes, proveedores y colaboradores, consultar información empresarial y ejecutar tareas operativas mediante conversaciones naturales.

El proyecto desarrollado para Inteligencia Jurídica demuestra la aplicación de estas capacidades en un servicio especializado de información legal.

---

<div align="center">

## Conecta con Oraneta

<a href="https://oraneta.com">
<img src="https://img.shields.io/badge/Sitio_Web-168BFF?style=for-the-badge" alt="Sitio web">
</a>

<a href="https://www.linkedin.com/company/oraneta/">
<img src="https://img.shields.io/badge/LinkedIn-643BFF?style=for-the-badge" alt="LinkedIn">
</a>

<a href="mailto:contacto@oraneta.com">
<img src="https://img.shields.io/badge/Contacto-C329F4?style=for-the-badge" alt="Contacto">
</a>

<br><br>

**Inteligencia artificial aplicada a procesos empresariales reales.**

**© 2026 Oraneta. Todos los derechos reservados.**

</div>
