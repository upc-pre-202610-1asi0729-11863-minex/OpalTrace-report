# Conclusiones

## Conclusiones y Recomendaciones

### Conclusiones

#### Sobre los Problem Statements y los resultados obtenidos

El primero de los Problem Statements planteaba que las empresas mineras sufren ineficiencias operativas al no poder monitorear en tiempo real el traslado de los minerales. Esta hipótesis quedó ampliamente validada durante el proceso de investigación: los tres entrevistados del segmento minero operaban con registros manuales en papel, plantillas de Excel o comunicación vía WhatsApp, sin ningún sistema integrado de trazabilidad. Efraín Zelaya describió cómo la falta de información precisa genera pérdidas significativas y un alto índice de fracaso en proyectos; Max Alonso Yapo identificó que los errores de pesaje, aunque pequeños en su origen, se acumulan y generan cuellos de botella operativos; y Rick Boris Guill documentó incidentes que tardan hasta una semana en reportarse. La arquitectura de OpalTrace, centrada en el registro digital de lotes, la transferencia de custodia verificada y el dashboard de Analytics en tiempo real, responde directamente a esta brecha. Los resultados de las entrevistas de validación confirmaron que la plataforma resuelve el problema en los tres perfiles: Rick completó en menos de tres minutos un reporte que en su operación actual toma una semana, y Max validó que las alertas de anomalía habrían prevenido los errores de pesaje que actualmente detecta con retraso.

El segundo Problem Statement señalaba que las joyerías no cuentan con mecanismos para validar el origen de los minerales, lo que afecta la credibilidad del distribuidor y genera pérdida de ventas. El análisis de entrevistas confirmó que este es uno de los quiebres más frecuentes del sector: Yesiliany gestionaba el inventario de forma completamente manual, Dante había perdido ventas directamente por no poder demostrar el origen del material a sus clientes, y Mauricio Perez vivió un incidente crítico con un proveedor que entregó material falsificado por ausencia de trazabilidad formal. La funcionalidad de certificación QR de OpalTrace, que vincula cada pieza de joyería con la cadena completa de trazabilidad del mineral, constituye la respuesta más directa a este problema. Los tres entrevistados del segmento validaron que la información incluida en el certificado responde exactamente a lo que sus clientes les preguntan antes de decidir una compra de valor.

El tercer Problem Statement abordaba que el consumidor final carece de medios para verificar si el producto que adquiere proviene de fuentes responsables. Esta problemática fue transversal a los tres entrevistados del segmento de consumidor: Carla, Mauricio Moquillaza y Oliver coincidieron en que su nivel de confianza en las marcas es bajo y que los métodos actuales de verificación (sellos de quilataje, consulta al vendedor) son insuficientes o fácilmente falsificables. La funcionalidad de escaneo QR para el consumidor final, que proporciona en segundos el recorrido completo del mineral desde la extracción hasta la joya, es el diferenciador más valorado por este segmento. Carla puntuó la experiencia con 9/10 y afirmó que la usaría activamente antes de cada compra; Oliver destacó que tener acceso a esta información en el punto de compra aumentaría significativamente su confianza.

---

#### Sobre los Assumptions y el comportamiento real de los segmentos

Los Business Assumptions establecieron que los usuarios del segmento minero necesitan una herramienta para validar el recorrido de los minerales y que el valor más importante para este segmento es la trazabilidad en tiempo real. Esta suposición se confirmó de manera contundente: el 100% de los entrevistados del segmento minero expresó que un sistema de rastreo digital desde la extracción sería altamente beneficioso o incluso esencial para sus operaciones. El assumption fue conservador, ya que la realidad mostró que la necesidad no es solo de monitoreo, sino de eliminación de la dependencia de registros manuales y comunicación informal como vector principal de información operativa.

El assumption que proyectaba que los clientes iniciales serían empresas mineras, joyerías y consumidores finales resultó preciso. Sin embargo, las entrevistas revelaron un matiz importante respecto a la heterogeneidad de los perfiles dentro del segmento minero: Efraín opera en minería informal en etapa de formalización, Max es jefe de metalurgia en una operación estructurada, y Rick es analista de control de proyectos con herramientas avanzadas como Power BI. Esta diversidad demanda que OpalTrace ofrezca interfaces diferenciadas por rol sin incrementar la complejidad del sistema para el usuario con menor experiencia digital.

El User Assumption que anticipaba que el quiebre de trazabilidad ocurre en el cambio de custodia del mineral fue uno de los más sólidamente validados. El análisis de entrevistas del segmento minero reveló que los errores y las pérdidas de información se concentran precisamente en los momentos de transferencia: de la mina a la planta, del turno entrante al saliente, del operador al supervisor. Esto orientó correctamente el énfasis arquitectónico en el bounded context de Custody Chain, cuyo mecanismo de transferencia verificada con firma digital y código QR está diseñado para actuar exactamente en esos puntos críticos de la cadena.

El assumption sobre la generación de ingresos mediante suscripciones mensuales escalonadas encontró respaldo en la recepción de los planes Silver, Gold y Platinum por parte de los tres segmentos durante las entrevistas de validación. Los entrevistados del segmento joyería, en particular Dante y Mauricio, mostraron disposición a asumir un costo por la plataforma si esta les permite evitar pérdidas de ventas por falta de certificación, lo que valida la elasticidad de precio proyectada en el modelo de negocio.

---

#### Sobre los Hypothesis Statements y los criterios de éxito

La primera hipótesis afirmaba que una plataforma que permita monitorear en tiempo real los minerales ayudará a reducir las pérdidas de recursos en las operaciones mineras. Las entrevistas de validación confirman cualitativamente la dirección de esta hipótesis: Max validó que el sistema de alertas de anomalía habría detectado los errores de pesaje que actualmente se acumulan sin control, y Rick demostró durante la sesión que el reporte de incidentes, que en su operación tarda una semana, se completó en la plataforma en menos de tres minutos. La validación cuantitativa del criterio de éxito —la reducción de pérdidas reportadas en los dashboards de Analytics— requiere una fase de operación real con datos de producción, la cual debe priorizarse en el roadmap inmediato post-lanzamiento.

La segunda hipótesis planteaba que una plataforma que certifique la autenticidad de los minerales mejorará la confianza entre joyerías y consumidores, medida cuando los productos con certificación sean más vendidos que los no certificados. Las entrevistas de validación con los seis usuarios de los segmentos de joyería y consumidor proporcionan evidencia cualitativa sólida: Dante afirmó que el certificado QR eliminaría las barreras de confianza que actualmente le cuestan ventas, y Carla señaló que la información de trazabilidad verificable en el punto de compra cambiaría completamente su decisión de adquisición. El criterio cuantitativo de ventas comparativas requerirá la instrumentación de un módulo de conversión una vez que la plataforma opere con usuarios reales en ambos segmentos.

La tercera hipótesis sostenía que una plataforma que proporcione información del origen del producto fomentará decisiones de compra responsables, medida a través del tiempo de visualización de la información de trazabilidad como estadística de engagement. Los tres entrevistados del segmento consumidor validaron que utilizarían activamente la funcionalidad de verificación QR antes de cada compra de joyería de valor. Oliver sugirió además añadir una representación visual del recorrido del mineral en forma de mapa interactivo, lo que indica que la información de trazabilidad tiene potencial de ser una experiencia de producto por derecho propio, no solo una utilidad de verificación. La métrica de tiempo de visualización es medible desde el primer release y debe activarse como evento de analítica en el bounded context de Consumer Experience.

---

#### Sobre los criterios de éxito del Lean UX Canvas

El criterio de negocio que proyectaba un crecimiento sostenido en la tasa de usuarios registrados mensualmente encuentra sustento en el tamaño del mercado identificado: más de 22 mil millones de soles en pérdidas anuales atribuidas a la falta de trazabilidad en el sector minero peruano, y una creciente demanda de certificación en el mercado de joyería urbana. El diferencial de OpalTrace —trazabilidad end-to-end integrada en una única plataforma SaaS frente a soluciones fragmentadas o software costoso e inflexible— representa una propuesta de valor no atendida que puede traducirse en captación de clientes insatisfechos con las alternativas actuales.

El criterio de reducir las ineficiencias operativas en el segmento minero es el más directamente alineado con los hallazgos de campo. El patrón de registro manual, error de acumulación y retraso en el reporte identificado en los tres entrevistados del segmento sugiere que OpalTrace debe enfocar sus métricas de adopción no en el uso pasivo de dashboards, sino en la sustitución activa del flujo de registro manual por el flujo digital: el número de lotes registrados a través de la plataforma frente a los reportes manuales procesados en paralelo es el indicador más revelador del cambio conductual real.

El criterio de conversión a planes superiores, con más del 10% de usuarios migrando del plan básico a planes de mayor funcionalidad, depende de que las capacidades de los planes Gold y Platinum demuestren valor tangible antes de que el usuario alcance el límite del plan de entrada. La generación automática de certificados PDF, el acceso al historial completo de trazabilidad y los dashboards avanzados de Analytics son las funcionalidades con mayor potencial de conversión según las preferencias expresadas en las entrevistas de validación, especialmente en el segmento de joyerías medianas y grandes empresas mineras.

---

### Recomendaciones

**Roadmap de producto a corto plazo (0–3 meses post-lanzamiento)**

La prioridad inmediata debe ser la instrumentación de métricas de adopción operativa. El criterio de éxito de la primera hipótesis —reducción de pérdidas en operaciones mineras— solo puede medirse si desde el primer día de operación se registran los eventos de registro de lotes, las alertas de anomalía generadas y las transferencias de custodia completadas por usuario y por operación. Se recomienda implementar un pipeline de analítica de comportamiento desde el sprint de lanzamiento.

La base de datos de tipos de minerales y parámetros de control debe ampliarse con las características propias de la minería peruana antes del lanzamiento público. Las entrevistas evidenciaron que los parámetros críticos difieren según el tipo de operación: Efraín trabaja con concentrados de polimetálicos, Max con tonelajes y leyes de mineral, y Rick con volúmenes de producción por zona. Incorporar los minerales y unidades de medida más frecuentes del sector minero nacional es una condición necesaria para que el módulo de Fleet Operations funcione con precisión en el mercado objetivo.

Se recomienda diseñar un flujo de incorporación (onboarding) diferenciado por rol dentro del segmento minero: operador de campo, jefe de turno, analista de control y gerencia de operaciones. El patrón identificado en las entrevistas muestra que el nivel de detalle requerido y las tareas prioritarias varían significativamente entre estos perfiles, y un onboarding único puede generar fricción inicial y abandono temprano.

**Roadmap de producto a mediano plazo (3–9 meses)**

La integración con sistemas de pesaje existentes en planta debe incorporarse al roadmap del plan Gold. Max identificó que sus errores operativos actuales provienen específicamente de la discrepancia entre las balanzas físicas y el registro manual posterior. Una integración directa con los sistemas de pesaje industriales mediante API o lectura de archivo eliminaría este punto de falla sin requerir cambio de comportamiento por parte del operador.

Se recomienda desarrollar una funcionalidad de modo offline para el registro de lotes en zonas con conectividad limitada. Efraín, que opera en una mina con acceso restringido a internet, señaló esta capacidad como una condición necesaria para la adopción en su contexto. La sincronización diferida de registros cuando el dispositivo recupera conectividad es técnicamente implementable en la arquitectura actual y ampliaría significativamente el alcance geográfico de la plataforma.

La expansión del módulo de Consumer Experience hacia una vista pública accesible sin registro previo debe considerarse como funcionalidad de alto valor para el segmento consumidor. Los tres entrevistados de este segmento utilizan el escaneo QR como primer punto de contacto con la plataforma; exigirles registro antes de visualizar la trazabilidad de una joya en el punto de venta es una barrera de fricción que puede derivar en abandono inmediato.

**Roadmap de producto a largo plazo (9–18 meses)**

El modelo de negocio SaaS debe explorar una oferta institucional orientada a empresas mineras formales de mediana escala que operan bajo marcos regulatorios específicos del Ministerio de Energía y Minas. OpalTrace puede posicionarse como la herramienta de trazabilidad que facilita el cumplimiento normativo y la generación de reportes para entidades regulatorias, generando un canal de distribución con menor costo de adquisición que el canal directo al consumidor y con mayor recurrencia en los ingresos.

Finalmente, se recomienda evaluar la incorporación de tecnología IoT para el registro automático de parámetros en los puntos de extracción y transferencia, eliminando la dependencia del registro manual incluso dentro de la plataforma. La integración de sensores de peso y geolocalización en los puntos críticos de la cadena representaría la evolución natural de OpalTrace hacia una solución de trazabilidad completamente automatizada, consolidando su diferencial frente a cualquier competidor que opere bajo un modelo de registro manual digitalizado.

---

## Video About-The-Team

El video **About-The-Team** de OpalTrace documenta el proceso de trabajo realizado por el equipo MINEX a lo largo del proyecto. Inicia con una reflexión grupal sobre el origen del problema: cómo garantizar la trazabilidad del mineral desde su extracción hasta el consumidor final en un sector caracterizado por registros manuales y baja digitalización. A continuación se desarrolla el proceso de diseño y arquitectura, mostrando cómo el equipo construyó un lenguaje común a través del Event Storming y definió los bounded contexts del sistema bajo un enfoque de Domain-Driven Design. Luego se documenta la etapa de implementación, abarcando el desarrollo del Landing Page, el frontend en Angular y el backend en Spring Boot con Spring Security y JWT, destacando la coherencia arquitectónica mantenida a lo largo de los tres sprints. El video concluye con el testimonio individual de cada integrante, describiendo las actividades realizadas, los outcomes logrados y las competencias desarrolladas durante el proyecto.

### Pauta de Secuencias de Contenido

| Sección | Inicio (hh:mm:ss) |
|---|---|
| Introducción | 00:00:00 |
| Contexto del proyecto | 00:01:00 |
| Proceso de trabajo | 00:02:15 |
| Testimonio — Armestar Felipa, Adrian Andres | 00:04:04 |
| Testimonio — Baldeon Vivar, Santiago Armando | 00:04:58 |
| Testimonio — Philco Mota, Katty Yolanda | 00:06:03 |
| Testimonio — Vergaray Calderon, Rose Almendra | 00:07:11 |
| Testimonio — Yi Torrejon, Ethan Raul | 00:08:29 |
| Cierre | 00:13:15 |

### URLs de Publicación

- **Microsoft Stream:** [About the Team](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241d159_upc_edu_pe/IQD00lqWD2JOQa_CsC5gzmxdAbaSzT7c77JT5Geu7fY6afE?e=oVzr0k)

- **YouTube:** [About the Team]()
