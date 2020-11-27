# <p align="center">IEEE TEST PLAN TEMPLATE</p>


# **Índice**

**1) Test Plan Identifier**

**2) References**

**3) Introduction**

**4) Test Items**

**5) Software Risk Issues**

**6) Features to be Tested**

**7) Features not to be Tested**

**8) Approach**

**9) Item Pass/Fail Criteria**

**10) Suspension Criteria and Resumption Requirements**

**11) Test Deliverables**

**12) Remaining Test Tasks**

**13) Environmental Needs**

**14) Staffing and Training Needs**

**15) Responsibilities**

**16) Schedule**

**17) Planning Risks and Contingencies**

**18) Approvals**

**19) Glossary**

**1 TEST PLAN IDENTIFIER**

| Versión | idProyecto | Nombre del Proyecto | Creador | Fecha de creación | Fecha de Revisión |
| --- | --- | --- | --- | --- | --- |
| 01 | HG202001 | Comunicación colmillo | Halcones Galacticos | 2020-11-27 |
 |

**2 REFERENCES**

Este documento está basado en el proyecto de Comunicación Colmillo el cual está descrito en el documento de Requerimientos.

**3 INTRODUCTION**

La comunicación entre alumnos, profesores y administrativos representa un problema la mayoría de las veces en la institución debido a los diferentes horarios de los estudiantes, la hora de atención de los profesores y las horas de las oficinas administrativas .

Para facilitar y disminuir este problema hemos desarrollado Comunicaciones Colmillo.

Esta aplicación será una nueva opción para que los alumnos, maestros y administrativos puedan comunicarse entre ellos de una forma segura, rápida y eficiente, logrando que tanto los maestros, como alumnos y directivos tengan una comunicación mas rápida y directa, por lo que ayudara mucho tanto para temas escolares, como para temas personales.

Comunicaciones colmillo no solo ayudará a que sea más rápido, sino también a que aquellos maestros que se les dificulta las otra aplicaciones como gmail o canvas, puedan comunicarse con sus alumnos sin tantos enredos, ya que la aplicación colmillo es parecida a cualquier red social, solo que diseñada únicamente para la Comunidad ITAM.

El objetivo de este documento es revisar el proceso de pruebas que se realizará para entregar un producto de calidad, tomando en cuenta el nivel de pruebas que se realizará y los involucrados en las diferentes partes del proceso.

**4 TEST ITEMS (FUNCTIONS)**

**5 SOFTWARE RISK ISSUES**

- El acceso a la base de datos del itam, considerando el acceso a los datos de inicio de sesión de cada usuario, así como los datos de cada alumno como materias y grupos inscritos, así como datos de administrativos.
- Fallas en los servidores del itam, lo que perjudica en nuestra aplicación por las bases de datos utilizadas.
- Manejo de concurrencia.
- Velocidad y fiabilidad de la recepción de cada mensaje,
- Interacciones de los usuarios, considerando el reglamento de alumnos
- Resolución e investigación de casos de acoso o deshonestidad académica.

**6 FEATURES TO BE TESTED**

-Creación de los grupos conforme a las materias inscritas en el semestre.

-Inicio de sesión utilizando los datos del itam, usuario y contraseña.

-Envío de archivos entre usuarios.
 -Búsqueda de usuarios.

-Mensajes administrativos sin restricciones.
 -Añadir usuario como contacto.

-Envío de mensajes.

-Subir archivos.

**7 FEATURES NOT TO BE TESTED**

El sistema no tendrá funciones que no sean probadas debido a que es un sistema nuevo. El sistema tendrá todas las funcionalidades óptimas condiciones para su primera versión.

**8 APPROACH (STRATEGY)**

Se iniciará el proceso de pruebas con la creación de un ambiente específico de pruebas, donde se probará cada feature por separado en un inicio con datos dummy es decir de prueba. Probando las funcionalidades individualmente y después en conjunto utilizando datos de prueba obtenidos de las interfaces y por último con usuarios y datos reales (prueba piloto).

1. Inicio de sesión:
  1. El inicio de sesión debe probarse específicamente contando con la conexión al servidor del ITAM con un usuario de prueba proporcionado por el ITAM.
  2. Se realiza prueba con usuarios durante prueba piloto con usuarios reales.
2. Búsqueda de usuario para enviar chat

1. Se prueba con datos locales de ejemplo para validar la funcionalidad.
2. Se realiza con datos de prueba obtenidos desde el servidor del ITAM.
3. Se realiza prueba con usuarios reales durante prueba piloto con usuarios reales.

3. Envío de chat

1. Se prueba funcionalidad individual de envío y recepción con usuarios prueba
2. Se prueba nivel de concurrencia en chats simultáneos por diferentes usuarios para evitar problemas de capacidad.
3. Se realiza prueba con usuarios obtenidos desde el servidor del ITAM.
4. Se realiza prueba con usuarios reales durante prueba piloto con usuarios reales.

**Las métricas del sistema son las siguientes:**

- Fecha y hora del pico de personas usando el sistema.
- ¿Falló el sistema en horarios con mucho tráfico?
- ¿Qué área es la más consultada, es decir, la que más mensajes recibe (administración, alumnos, docentes)?¿ Necesita mayor alcance?
- ¿Cuáles de las funcionalidades tienen mejores evaluaciones de los usuarios?
- ¿Cuáles de las funcionalidades tienen las peores evaluaciones de los usuarios? ¿Por qué?
  - ¿Los motivos cambian principalmente por carrera o por tipo de usuario?

Cada una de las métricas anteriores buscan analizar el comportamiento y la funcionalidad que cada tipo de usuario le da a las diferentes partes del sistema y analizar cuáles resultan ser las mejores para mejorarlo. Así mismo el enfoque que se les da es para un autocrecimiento y una adherencia de los estudiantes, profesores y administrativos al este.

Para mantener la integridad del sistema a lo largo del tiempo las pruebas se realizan rigurosa y exhaustivamente cada semestre o bien cada vez que una de las métricas se encuentre debajo de los niveles esperados.

El sistema tiene tres tipos de usuarios distintos: alumnos, profesores y administrativos. Las configuraciones se prueban por cada tipo de usuario, es decir se tienen tres tipos de configuraciones.

Hardware

Software

Combinations of HW, SW and other vendor packages

What levels of regression testing will be done and how much at each test level?

Will regression testing be based on severity of defects detected?

How will elements in the requirements and design that do not make sense or are untestable be processed?

**9 ITEM PASS/FAIL CRITERIA**

Se considera que cada sección es correcta cuando las funcionalidades establecidas en cada sección funciona de forma esperada, para poder entregar y declarar como terminada una sección debe pasar la diferentes pruebas que se especifica en cada una.

Se debe cumplir con el 100% de funcionalidad para que se pueda dar por concluido el proceso.

Es posible que existan errores que se presenten durante el uso de la plataforma, que no sean detectados durante las pruebas.

Deben estar cubiertos todos los casos de uso de forma correcta y cubiertas todas las pruebas.

En caso de que se presenten errores durante las pruebas deben ser corregidos y testeados nuevamente desde cero para validar la corrección del mismo.

**10 SUSPENSION CRITERIA AND RESUMPTION REQUIREMENTS**

Errores en cada una de las fases de pruebas de los feautures detienen las pruebas de la siguiente fase de esa sección, no se avanza a pruebas con datos reales si no pasa la prueba de datos locales.

Cada feature debe ser probado por completo de forma individual y en conjunto con los demas en todas sus fases.

**11 TEST DELIVERABLES**

Se entregará al cliente :

- El presente documento
- Los casos de prueba .
- Los resultados de las pruebas iniciales.
- Registro de errores generados en las pruebas.
- Reporte de acciones correctivas de los errores encontrados.
- Resultados finales después de las correcciones

**12 REMAINING TEST TASKS**

No aplica ya que todos los tasks están cubiertos en el plan inicial de testing de los features,

**13 ENVIRONMENTAL NEEDS**

Se necesita en un inicio un ambiente de pruebas donde se realizarán todas las pruebas funcionales del sistema.

En este ambiente de pruebas es necesario tener acceso a la base de datos de usuarios del ITAM con datos dummy para realizar pruebas en los módulos de inicio de sesión y obtención de información de cada usuario. Para probar que la conexión y obtención de información.

A su vez es necesario un simulador de concurrencia para probar el nivel estabilidad y disponibilidad del sistema para el número de usuarios solicitados.

El envío y recepción de chats se probará en un inicio con usuarios de prueba de forma &quot;local&quot; con usuarios prueba.

**14 STAFFING AND TRAINING NEEDS**

El sistema es muy intuitivo y simple, por lo que no creemos que se necesite capacitación alguna en el uso, a excepción de maestros o administrativos de edad avanzada que tengan dificultad con el manejo de nuevos aparatos tecnológicos y sus funcionalidades.

La necesidad de capacitación en términos de manejo del sistema se cubrirá por medio de material gráfico como tutoriales y video tutoriales.

**15 RESPONSIBILITIES**

|
 | TM | PM | DEV TEAM | TEST TEAM | CLIENT |
| --- | --- | --- | --- | --- | --- |
| Aceptación de documentación de pruebas | x | x |
 | x | x |
| Revisiones de diseño de sistema | x | x | x | x | x |
| Procedimientos de pruebas | x | x | x | x |
 |
| Revisión de prototipos de pantallas |
 |
 | x | x | x |
| Control de cambios | x | x | x | x | x |

**16 SCHEDULE**

|
 | Alumnos | Profesores | Administrativos |
| --- | --- | --- | --- |
| 3 semanas | Vinculación con la base de datos de alumnos del ITAM.
Inicio de sesión SSO.
Pruebas de inicio de sesión. | Vinculación con la base de datos de profesores del ITAM.
Inicio de sesión SSO
Pruebas de inicio de sesión | Vinculación con la base de personal administrativo del ITAM.
Inicio de sesión SSO.
Pruebas de inicio de sesión |
| 2 semanas | Contraseñas
Pruebas de contraseñas (confiabilidad, vinculación con las credenciales de la página del ITAM (p.e. canvas, comunidad), cambios, etc) | Contraseñas
Pruebas de contraseñas (confiabilidad, vinculación con las credenciales de la página del ITAM (p.e. canvas, comunidad), cambios, etc) | Contraseñas
Pruebas de contraseñas (confiabilidad, vinculación con las credenciales de la página del ITAM (p.e. canvas, comunidad), cambios, etc) |
| 3 semanas

 | Búsqueda de otros usuarios.
Pruebas de búsquedas de usuario (perfil completo de los usuarios ) | Búsqueda de otros usuarios.
Pruebas de búsquedas de usuario (perfil completo de los usuarios.) | Búsqueda de otros usuarios.
Pruebas de búsquedas de usuario (perfil completo de los usuarios) |
| 2-3 semanas | Crear nuevas conversaciones.
Eliminar conversaciones.
Pruebas de creación de conversaciones (sin contenido.) | Crear nuevas conversaciones.
Eliminar conversaciones.
Pruebas de creación de conversaciones (sin contenido.) | Crear nuevas conversaciones.
Eliminar conversaciones.
Pruebas de creación de conversaciones (sin contenido.) |
| 3-4 semanas | Enviar y recibir mensajes.
Enviar contenido multimedia (mensajes de voz, imágenes, videos, etc.)
Enviar contenido adjunto (documentos, presentaciones, etc.)
Pruebas de mensajes (Revisar si los mensajes llegaron correctamente o no, etc.) | Enviar y recibir mensajes.Enviar contenido multimedia (mensajes de voz, imágenes, videos, etc.)
Enviar contenido adjunto (documentos, presentaciones, etc.)
Pruebas de mensajes (Revisar si los mensajes llegaron correctamente o no, etc.) | Enviar y recibir mensajes.
Enviar contenido multimedia (mensajes de voz, imágenes, videos, etc.)
Enviar contenido adjunto (documentos, presentaciones, etc.)
Pruebas de mensajes (Revisar si los mensajes llegaron correctamente o no, etc.) |
| 2-3 semanas | Listas de conversaciones.
Pruebas de esta sección (el usuario puede ver sus conversaciones activas, inactivas,etc.) | Listas de conversaciones.
Pruebas de esta sección (el usuario puede ver sus conversaciones activas, inactivas,etc.) | Listas de conversaciones.
Pruebas de esta sección (el usuario puede ver sus conversaciones activas, inactivas,etc.) |
| 5-6 semanas | Chats grupales:\*Grupos en los que está matriculado \*Creación de grupos propios. Pruebas de chats grupales (el alumno no puede eliminar al profesor, etc.) | Chats grupales:\*Grupos en los que imparten clases \*Creación de grupos propios.
Pruebas de chats grupales (el profesor no puede eliminar a un alumno, etc.) | Chats grupales:\*Creación de grupos propios.
Pruebas de chats grupales (formación de grupos, eliminar alumnos que se dieron de baja, etc.) |
| 3 semanas | Reportes y bloqueos de usuarios.
Pruebas de reportes de usuarios. | Reportes y bloqueos de usuarios.
Pruebas de reportes de usuarios. | Reportes y bloqueos de usuarios.
Pruebas de reportes de usuarios. |
| 5-6 semanas | Pruebas exhaustivas de seguridad y confiabilidad de todo el sistema en conjunto.
Pruebas de todo el sistema. |

**17 PLANNING RISKS AND CONTINGENCIES**

-Pruebas con menores impactos que los reales

-Pruebas con equipos que no soporten la carga necesaria para las pruebas

-Retraso en la entrega del sistema

-Cambios por parte de la institución que hará uso de ella

-Cambios en la cantidad de usuarios que harán uso de ella

-El proyecto debe entregarse 15 días antes de la fecha prevista a los encargados de pruebas, por lo que tendremos ese margen en caso de algún inconveniente en procesos anteriores.

-Las pruebas se harán hasta llegar al máximo de usuarios procesables por el sistema para no estar limitados por los usuarios que la institución plantea.

-La institución tendrá una fecha límite para la entrega de cambios mayores y menores, en caso de ser necesario cambios mayores o menores fuera de la fecha, la entrega se retrasara y el costo se reevaluará..

**18 APPROVALS**

El encargado de cada sección tendrá que aprobar la subparte del sistema de la que se encarga, después el encargado del proyecto deberá verificar que cumpla con todos los requisitos y que las pruebas necesarias se pasaran con éxito y finalmente la institución debe aprobar el sistema y en caso de algún problema se evaluará de donde proviene y quienes son los responsables para repararlo.

**19 GLOSSARY**

No aplica
