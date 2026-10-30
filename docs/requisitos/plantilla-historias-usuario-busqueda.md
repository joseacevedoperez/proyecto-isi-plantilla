# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [dd/mm/aaaa] |
| Versión | [Versión de trabajo] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como usuario de la plataforma, quiero localizar recetas que se ajusten a mis necesidades alimentarias mediante criterios de búsqueda y consultar su información, para encontrar recetas adecuadas a mis preferencias.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

US-01 – Configuración y ejecución de la búsqueda: permite introducir palabras o frases y seleccionar ingredientes que se desean incluir o excluir.
US-02 – Consulta de resultados y detalle: permite visualizar las recetas encontradas y consultar toda su información.
US-03 – Gestión de búsquedas sin resultados y fallos: permite recibir sugerencias cuando no existen coincidencias y conocer los problemas que impiden completar una consulta.

## US-01

**Título:** Búsqueda de recetas mediante palabras o frases.

Como usuario de la plataforma,
quiero buscar recetas introduciendo palabras o frases,
para encontrar recetas que se ajusten a mis necesidades y preferencias.

**Fuentes:** UR-08: Búsqueda de recetas.
             FR-085: Búsqueda mediante palabras clave o frases.
             Acta de acuerdos UC-21, versión 1.1.

### Criterios de aceptación

CA-01. Introducción de texto: Dado que el usuario accede a la búsqueda, cuando introduce una palabra o frase, entonces el sistema permite utilizarla como criterio de búsqueda.
CA-02. Búsqueda de coincidencias: Dado que el usuario introduce un texto, cuando ejecuta la búsqueda, entonces el sistema busca coincidencias en el título y en la descripción breve de las recetas, sin distinguir entre mayúsculas y minúsculas.
CA-03. Búsqueda de frases: Dado que el usuario introduce una frase, cuando ejecuta la búsqueda, entonces el sistema busca la frase respetando el orden de las palabras.

## US-02

**Título:** Visualización de recetas encontradas.

Como usuario de la plataforma,
quiero visualizar los resultados de mi búsqueda y acceder al detalle de cada receta,
para conocer sus características y decidir cuál se adapta mejor a mis necesidades.

**Fuentes:** UR-08: Búsqueda de recetas.
             FR-089: Visualización de resultados con información de cada receta.
             FR-099: Ordenación por fecha de publicación.
             Acta de acuerdos UC-21, versión 1.1.

### Criterios de aceptación

CA-01. Visualización de resultados: Dado que existen recetas que cumplen los criterios de búsqueda, cuando el sistema muestra los resultados, entonces únicamente aparecen recetas publicadas y validadas, ordenadas de más reciente a más antigua.
CA-02. Información de las recetas: Dado que el sistema muestra los resultados, cuando el usuario consulta el listado, entonces cada receta presenta su título, imagen, calificación promedio y descripción breve. Si no dispone de imagen o valoraciones, se indica "Sin imagen" o "Sin valoraciones", respectivamente.
CA-03. Consulta del detalle: Dado que el usuario selecciona una receta, cuando accede a su detalle, entonces el sistema muestra el título, imagen si existe, ingredientes, instrucciones de preparación, tiempo de cocción, número de porciones, autor y fecha de publicación, así como la insignia de validación cuando corresponda.

## US-03

**Título:** Selección de ingredientes y gestión de búsquedas sin coincidencias.

Como usuario de la plataforma,
quiero seleccionar ingredientes que deseo incluir o excluir en mis búsquedas y recibir sugerencias cuando no encuentre resultados,
para ajustar mejor las recetas a mis preferencias y encontrar alternativas adecuadas.

**Fuentes:** UR-08: Búsqueda de recetas.
             FR-086: Búsqueda mediante ingredientes seleccionados.
             FR-087: Exclusión de ingredientes.
             FR-095: Combinación de múltiples criterios de búsqueda avanzada.
             Acta de acuerdos UC-21, versión 1.1.

### Criterios de aceptación

CA-01. Selección de ingredientes: Dado que el usuario configura una búsqueda avanzada, cuando selecciona ingredientes para incluir o excluir, entonces el sistema utiliza estos criterios para filtrar las recetas, mostrando aquellas que contienen todos los ingredientes incluidos y ninguno de los excluidos.
CA-02. Búsqueda sin resultados: Dado que ningún resultado cumple los criterios establecidos, cuando finaliza la búsqueda, entonces el sistema informa de que no se han encontrado recetas y propone correcciones ortográficas o alternativas relacionadas cuando estén disponibles.
CA-03. Gestión de errores: Dado que se produce un fallo durante la búsqueda, cuando el sistema no puede completar la consulta, entonces informa al usuario del problema y le permite volver a intentarlo.

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
