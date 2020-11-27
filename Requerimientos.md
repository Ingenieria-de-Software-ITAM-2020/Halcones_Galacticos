
**Especificación de requisitos de software para Sistema de comunicaciones del ITAM**  
**Versión 1.0 aprobada**


**1.Introducción**  
**1.1.          Propósito**   
Crear una aplicación que facilite la comunicación entre los estudiantes, el personal académico y el personal administrativo del ITAM. Es indispensable que el proyecto cumpla con los estándares de calidad apropiados, considere las necesidades de los alumnos y cumpla con los valores del instituto.
La comunicación entre los estudiantes, los profesores y personal académico se dificulta debido a los diferentes horarios de cada uno de ellos, este sistema pretende proveer un ambiente de comunicación ágil y flexible, creando un entorno ameno y más cercano para la comunidad del ITAM. Con este propósito se integra este proyecto, tomando en cuenta estándares de UX, así como los más altos paradigmas de calidad.


**1.2.          Convenios de documentos**  
El sistema es completamente nuevo, por lo que se tiene que adaptar el proyecto a las normas de los sistemas existentes del instituto, en particular a las políticas del ITAM correspondientes al  reglamento de alumnos, así como a los protocolos del personal administrativo. \

**1.3.          Audiencia prevista y sugerencias de lectura**  
Este documento está dirigido al equipo de desarrolladores encargado de llevar a cabo el sistema de comunicaciones para los alumnos del ITAM. Para este proyecto solo es necesaria la lectura del presente documento en orden cronológico.  

**1.4.          Alcance del producto**  
El sistema de comunicación para los alumnos del ITAM es una aplicación web diseñada para que los estudiantes puedan comunicarse con mayor facilidad entre ellos, con sus profesores y con el departamento de servicios académicos. Consolidando de manera eficiente a la comunidad ITAMI
Considerando poder mandar mensajes de texto, imágenes y distintos tipos de archivos multimedia para poder comunicarse entre ellos.

**2.               Descripción general**  
**2.1.          Perspectiva del producto**    
El sistema está basado en los sistemas de comunicación más efectivos que conocemos, entre ellos whatsapp y messenger (de facebook), pero está adaptada especialmente a las necesidades del alumno y a los principios y reglas de la institución.

**2.2.     Funciones del producto**  
Las funciones principales que el sistema descrito contiene, a grandes rasgos, son las siguientes: 
Permitir a los alumnos buscar a otros usuarios en la plataforma (alumnos, profesores y administrativos).
Permitir a los profesores buscar a alumnos dentro de la plataforma, enfatizando a aquellos que están inscritos en un grupo en particular.
Permitir mandar mensajes entre los usuarios de la plataforma.
Crear chats grupales para facilitar la comunicación entre el grupo y entre equipos de trabajo.
Ver una lista de las conversaciones pasadas, filtradas por semestre.
Procurar que las conversaciones cumplan el reglamento del instituto ( Se permite reportar todas las conversaciones que se consideren inapropiadas).  

**2.3.          Clases y características de usuario**  
El sistema de comunicaciones colmillo será usado por 3 tipos de usuarios distintos: alumnos del ITAM, profesores y personal académico.
Los alumnos se distinguen por ser la cuenta con más funciones y libertades, son capaces de contactar a otros alumnos, maestros y académicos (siempre y cuando sigan algunas condiciones necesarias para su interacción). El objetivo es facilitar la comunicación entre este tipo de usuarios, así como ponerlos en contacto con personal del instituto. La aplicación solventa todas las necesidades de comunicación que se relacionen con las actividades académicas de un estudiante.
Los profesores y personal administrativo tienen una interacción limitada con los usuarios de la plataforma. En el caso de los profesores, solo permiten el contacto con los alumnos de sus grupos de clase, para esto, la aplicación se enfoca en permitir que el profesor comunique de manera clara los mensajes del curso y que resuelva dudas de manera eficiente. En el caso del personal administrativo, permite que se comuniquen solo con alumnos y que notifiquen en caso de ser necesario a la comunidad o a un alumno en particular.  

**2.4.          Entorno operativo**  
Para comenzar operaciones es necesario un servidor robusto con certificados de seguridad. 
Es necesario que el dispositivo que va a acceder a la aplicación cuente con una conexión a internet. Para hacer uso de nuestra página se requiere un navegador web estable (de preferencia actualizado), se recomienda usar Firefox, Google Chrome, Safari, Microsoft Edge, u Opera.   

**2.5.          Restricciones de diseño e implementación**  

Se deben considerar en primera instancia las políticas de privacidad ya que la aplicación va a hacer uso de información sensible de cada alumno, en especial a las contraseñas y en un futuro información académica del usuario.

También es importante asegurar la aplicación pues debe de cumplir con los estándares de calidad, en especial de Integridad, pues de esto depende el uso correcto de la cuenta e identidad de cada uno de nuestros usuarios (alumnos, profesores y personal administrativo). A su vez se debe considerar a detalle la cantidad de accesos que habrá a la plataforma y la gran cantidad de tráfico que va a haber de mensaje probablemente en horas de trabajo universitario.

**2.6.          Documentación del usuario**   

Sección de preguntas frecuentes.
- Manuales de usuario:
- Alumno 
- Profesor 
- Administrativos
- Datos de contacto para soporte técnico.   

**2.7.          Suposiciones y Dependencias**  
Este sistema depende de varios servicios del ITAM, en particular los de inicio de sesión e información académica de los alumnos y de los profesores para filtrar los usuarios a los que tienen acceso. Debido a esto se supone que se tiene acceso al servicio de autenticación de alumnos del ITAM, así como a servicios de información académico.   

**3.               Requerimientos de interfaz**     
**3.1.          Interfaces de usuario**  
1. Inicio de sesión

   - Usuario (TextField): este textField se utilizara con formato de texto para que el usuario ingrese su nombre de usuario de la aplicación. El placeholder debe indicar que se trata de un campo de “Usuario”.
   - Contraseña (TextField): este textField se utilizara con formato de contraseña para que el usuario ingrese la contraseña que corresponde con el usuario y conforme vaya escribiendo, esta se irá ocultando marcando únicamente círculos. El placeholder debe indicar que se trata de un campo de “Contraseña”.
   - Olvidé mi contraseña (Link): este botón lo usaremos para que en caso de que el usuario haya olvidado su contraseña pueda mandarlo a otra página para recuperarla.
Ingresar (Button): Este botón nos llevará a la página del chat de la aplicación de nuestro usuario.
![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/1.png "Optional Title") 


1. Recuperar contraseña

   - Correo (TextField): dentro de este Textfield tendrás que agregar el correo utilizado para enviarte un link de recuperación de contraseña.
   - Recuperar contraseña (Button): Este botón se encargará de tomar el correo al que se mandara el link, mandara la instrucción de enviar correo y a continuación te mandara a la pantalla de inicio de sesión.
![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/2.png "Optional Title")




1. Pantalla principal: Chat

   - Contactos (List): este componente se utilizará para tener las conversaciones recientes, en el podrás seleccionar la conversación que deseas ver. Cada miembro de la lista tiene el nombre del contacto y un pequeño icono del lado izquierdo que nos dará a entender si es un alumno, un grupo, un administrativo o un maestro. En este panel también se puede ver los usuarios que te han mandado solicitud de conversación.
   - Lupa (Button): este se utilizara para mandarnos a otra página donde podremos buscar a nuevos usuarios.
   - “+” (Button): este botón nos abrirá un popup en la ventana, en esta podremos elegir a los usuarios que queremos agregar a un grupo.
   - Mensaje (TextField): habrá un textfield que se utilizará como cuadro de texto en el que podremos escribir nuestros mensajes a enviar.
   - Enviar (Button): este botón se encontrará del lado derecho junto al textfield de mensaje y se encargará de tomar el texto escrito en el textfield y enviarlo, así como borrar lo que se encuentra en textfield para que la persona pueda enviar más.
   - Agregar archivos (Button): Este botón abrirá una pequeña ventana donde el usuario puede cargar archivos desde su dispositivo electrónico.
   - Usuario (Button): al presionar este botón se desplegará un menú de usuario, actualmente solo posee la opción de cerrar sesión.
   - Usuario (Button): este botón al presionarlo nos mostrara la opción para cerrar sesión
   ![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/3.png "Optional Title")
   
1.Ventana secundaria: Grupo

   - “+” (Button): Este botón abre la pestaña para seleccionar a los usuarios que se desea agregar a un chat grupal, únicamente aparecen en la lista los usuarios que han sido agregados previamente o que forman parte del mismo salón de clases.
   - Crear (Button): Este botón creará un grupo nuevo después de haber seleccionado a los usuarios que deseamos agregar al grupo.
   ![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/5.png "Optional Title")
   
1. Ventana secundaria: Selección de archivos

   - Adjuntar archivo (Button): Este botón abrirá una pantalla del explorador de archivos de tu equipo para que puedas seleccionar el archivo que deseas subir, cuando lo selecciones, comenzará a cargar el archivo y será enviado una vez que haya sido cargado.
   ![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/9.png "Optional Title")
   
1. Pantalla secundaria: BÚsqueda

   - Buscador (TextField): este se utilizara para escribir el nombre del usuario a buscar, se tendrá que escribir el nombre en este textfield para poder posteriormente presionar el botón de “Buscar”.
   - Tipo de usuario (Radio List): en esta lista de radio buttons se puede seleccionar el tipo de usuario que buscas, para filtrar y mostrar los resultados más relevantes. Aparte de los resultados exactos, se muestra una lista de usuarios que coinciden de alguna forma con el criterio de búsqueda.
   - Buscar (Button): el botón nos ayudará a cuando terminemos de escribir el nombre poder comenzar a buscar tomando en cuenta tanto el nombre a buscar, como el tipo de usuario que designamos como prioridad.
   - Mandar mensaje(Button): Este botón lo tendremos como opción en cada usuario para mandarle solicitud de amistad.
   ![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/6.png "Optional Title")
   
1. Ventana secundaria: Solicitud

   - Ventana: Cuando selecciones a un usuario para mandarle solicitud de conversación, aparecerá una ventana que confirmará el estatus del envío de la solicitud hacia esa persona.
   - Aceptar (Button): el botón aceptar únicamente cerrará la ventana de confirmación de solicitud enviada.
   ![Alt text](https://github.com/Ingenieria-de-Software-ITAM-2020/Halcones_Galacticos/blob/main/Imagenes/7.png "Optional Title")





**3.2.          Hardware Interfaces**  
El producto es una aplicación web, por lo que el único componente físico necesario para su correcto funcionamiento es el servidor en el cual va a estar almacenada la aplicación. Se hará uso de los servidores dados por el ITAM, o en su defecto, servidores privados capaces de soportar el tráfico elevado del sistema.\

**3.3.          Software Interfaces**  
Las conexiones que existirían entre nuestro sistema con otros, sería con el sistema de inicio de sesión que se utiliza para comunidad (SSO).  Es necesario conocer toda la información de los alumnos así como las materias a las que está inscrito para de esta forma poder generar los grupos de chat a los que cada alumno podrá tener acceso por default, así como mandar mensaje directamente a sus profesores. A su vez es importante conocer el organigrama interno de las distintas áreas del ITAM para de esta forma poder mandar un mensaje a las distintas áreas administrativas.


**3.4.          Interfaces de comunicaciones**  

Para el funcionamiento adecuado de la plataforma se necesita:  

- Un servidor capaz de soportar el tráfico elevado del sistema (con velocidad y demanda escalable).
- Certificado TSL para el encriptado usuario-servidor.
- Certificado SSL para cada transacción.
- Se necesitan protocolos de concurrencia y de mensajes en tiempo real para evitar problemas de Integridad.
- Acceso al API de la institución para consultar la información de los usuarios, profesores, grupos y materias.


**4.               Características del sistema  
4.1. REQ-1 : Buscar a otros usuarios de la plataforma**  

**4.1.1 Descripción y prioridad**  
Cada usuario puede buscar a otros usuarios respetando las normas de privacidad establecidas por la institución (p.e. no se tiene contacto directo con el rector, o bien con personal docente ajeno a la carrera en curso), las personas que aparecen en la búsqueda se determinan en función a los grupos y el rol de usuario. 
Algunas de las consideraciones de privacidad se describen a continuación: 
- El alumno puede buscar a otros alumnos, priorizando en la búsqueda a las personas que pertenezcan a su grupo (la búsqueda es por nombre de usuario); puede buscar a un profesor (por departamento o por nombre, dando prioridad a los profesores de los grupos en los que está inscrito); y, puede buscar a un miembro del personal administrativo (por área a la que pertenece).
- Las cuentas de profesores y del personal académico prioriza la búsqueda de alumnos (por grupo, nombre o clave única), en especial aquellos alumnos que pertenecen al mismo grupo.
Este requerimiento tiene una prioridad alta, pues es necesario que los usuarios puedan encontrar a otros miembros del instituto para mandarles mensajes.

**4.1.2 Secuencias de estímulo/respuesta**  
El usuario hace click en el botón de “Buscar”, posteriormente filtra el tipo de usuario que desea contactar y realiza la búsqueda.

**4.1.3 Requisitos funcionales**  
- Detalles
   - Alcance: Que cada usuario pueda buscar a otros usuarios en la plataforma.
   - Prioridad: Alta.
   - Nivel: Cuenta de alumnos, profesores y personal administrativo.
   - Condiciones: Haber iniciado sesión y hacer click en el botón correspondiente.
- Consiste en: 
   - Habilitar la funcionalidad de búsqueda de usuarios a cada tipo de perfil, se deben considerar las restricciones de privacidad pertinentes (oportunidad de mandar solicitud de mensaje si esa persona no tiene relación directa con el usuario).
   - Los alumnos tienen la posibilidad de filtrar la búsqueda.
   - Un botón de “Buscar”, y una lista que contenga los resultados de búsqueda.
- Escenario de éxito:
   - El usuario escribe los datos necesarios para la búsqueda y obtiene como resultado una lista que contiene al usuario correspondiente.
- Escenario de errores:
   - No existe ningún usuario que posea los datos introducidos, en este caso se despliega el mensaje de error correspondiente.
- Casos de uso: 
   - El alumno busca a otros alumnos priorizando los que estén en su mismo salón (por nombre).
   - El alumno busca a un profesor (por departamento o por nombre).
   - El alumno busca a un miembro del personal administrativo (por departamento).
   - El profesor y el personal administrativo pueden buscar alumnos (por grupo, nombre o clave única).
La búsqueda del profesor prioriza a los alumnos que están inscritos en alguna de sus clases.

**4.2. REQ-2 : Mandar mensajes**  

**4.2.1 Descripción y prioridad**  
Consiste en que cada usuario pueda mandar mensajes a otros usuarios una vez que ha encontrado el perfil (en cada perfil hay un botón de “Enviar mensaje”). 
La comunicación es entre alumnos,  profesores y personal del departamento administrativo. En caso de que un usuario quiera mandar un mensaje a alguien que no tenga relación directa (que no esté inscrito en el mismo grupo de una materia en particular), puede mandar una solicitud para iniciar la conversación (Por lo que sólo se iniciará una conversación entre 2 usuarios si ambos están de acuerdo).

Los detalles importantes que se tienen que tomar en cuenta son que:

- Sea posible  mandar mensajes de texto o archivos adjuntos (imágenes, documentos, etc.).
- Los usuarios (alumnos y profesores) puedan deshacer el envío de mensajes en el primer minuto de envío.
- El profesor puede marcar un mensaje como “anuncio importante” (mensajes que informan acerca de exámenes, bajas, calificaciones, revisiones, etc.) en los chats grupales.
- Este requerimiento tiene una prioridad alta, pues es la funcionalidad principal de la aplicación.

**4.2.2 Secuencias de estímulo/respuesta**  
Una vez que el usuario ha encontrado al usuario que desea contactar, hace click en el botón correspondiente para enviar un mensaje. Esto abre la conversación entre los dos usuarios, donde se puede redactar y enviar el mensaje.


**4.2.3 Requisitos funcionales**  
- Detalles
  - Alcance: Que todos los usuarios puedan mandar mensajes
  - Prioridad: Alta
  - Nivel: Todos los usuarios de la plataforma (alumnos, profesores y personal administrativo)
- Condiciones: Iniciar sesión y que ambos usuarios estén en el mismo grupo o tengan un acuerdo mutuo de comunicación.
Consiste en:
- Una pantalla que contenga la conversación entre los individuos que se quieren comunicar.
- Implementar comunicaciones por mensaje en tiempo real (Como messenger y whatsapp).
- Mensaje de solicitud de iniciar una conversación.
Escenario de éxito:
- Todos los usuarios son capaces de redactar, enviar y recibir mensajes de distintos usuarios.
Escenario de errores:
- En caso de no tener conexión a internet, se van a mandar los mensajes tan pronto se restablezca la conexión.
- En caso de intentar cerrar la pestaña mientras que aún no se envían los mensajes, se va a notificar al usuario para que decida si quiere abandonar la página o no.
- En caso de no tener permiso de contactar al otro usuario, notificar al usuario que no cuenta con el permiso de hablar con la otra persona.






**4.3. REQ-3 : Lista de conversaciones**  

**4.3.1 Descripción y prioridad**  
Los usuarios pueden ver su lista de conversaciones, estas incluyen: Conversaciones activas o con nuevos mensajes, conversaciones previas (organizadas por antigüedad, separadas por semestre) y solicitudes de mensajes (En caso de que un profesor quiera contactar a un alumno de otro grupo.

Detalles importantes:

- Los usuarios pueden activar o desactivar notificaciones de la conversación que desee.
- Las conversaciones pueden ser archivadas. 
- El usuario puede reportar una conversación para someterla a revisión (En caso de que alguien mande contenido inapropiado o tenga una conducta que vaya en contra de los principios del instituto).
- La lista debe facilitar ver las solicitudes de mensajes.

Ver la lista de conversaciones activas tiene prioridad alta, debido a que es parte del MVP y sin la lista no es posible cambiar de conversaciones ni ver mensajes pasados. 
Las funcionalidades como las notificaciones y archivar conversaciones activas tienen prioridad media, pues mejoran la interfaz del usuario, pero no tiene que ser parte del MVP.

**4.3.2 Secuencias de estímulo/respuesta**    
Debido a la importancia y a lo frecuente que se puede realizar esta acción, la lista de contactos se muestra todo el tiempo en la interfaz una vez que el usuario ha iniciado sesión.
Si el usuario hace clic en una conversación (en el panel lateral que contiene las conversaciones abiertas), se muestra la conversación con ese usuario.

**4.3.3 Requisitos funcionales**  
- Detalles
   - Alcance: Mostrar una lista de conversaciones abiertas en un panel lateral izquierdo. Es necesario mostrar las notificaciones, dar la posibilidad de reportar el chat por abuso, silenciar las notificaciones de usuario y permitir que el usuario archive la conversación .
   - Prioridad: Alta (la lista de conversaciones) y Media (Funcionalidad extra).
   - Nivel: Todos los usuarios (Alumnos, profesores y departamento administrativo).
   - Condiciones: Iniciar sesión y pertenecer a un grupo o tener consentimiento de comunicación.
- Consiste en:
   - Un panel lateral con la lista que contiene todas las conversaciones activas y previas.
   - Que cada conversación notifique al usuario la cantidad de mensajes nuevos.
   - En los settings de la conversación dar la capacidad de mutar.
   - En los settings de la conversación dar la capacidad de reportar (En caso de conducta inapropiada por alguna de las partes).
   - Organizar las conversaciones por fecha y separar las conversaciones por semestre.


Escenario de éxito:
- El usuario puede ver la lista de conversaciones previas.
- Puede entrar a cualquier chat de su lista para redactar, enviar y recibir mensajes.
- En caso de ser necesario puede silenciar o reportar una plática.
Escenario de errores:
- En caso de no contar con conexión a internet se va a guardar las acciones realizadas por el usuario y se va a esperar a la reconexión para efectuarlas.
- En caso de que el usuario intente dejar la pestaña, se notificará a los usuarios que no se han efectuado las acciones, para que ellos decidan si quieren esperar o abandonar la página.




**4.4. REQ-3 : Chat Grupales**  

**4.4.1 Descripción y prioridad**  
Esta funcionalidad permite a los alumnos y profesores crear chats grupales, también genera automáticamente un chat grupal que contiene a todos los alumnos de un curso, así como al profesor correspondiente. Por lo tanto este módulo va a permitir que múltiples usuarios interactúen entre sí.

Detalles importantes:

- Los usuarios administradores pueden cerrar los grupos que están archivados.
- Los usuarios pueden salirse de los grupos a los que no quieran pertenecer.

Esta funcionalidad tiene una prioridad media, debido a que aunque es importante y pertenece al MVP, no es crucial para el funcionamiento de la plataforma.
 
**4.4.2 Secuencias de estímulo/respuesta**  
Para crear una conversación grupal el usuario hace selecciona la opción de crear un nuevo grupo y posteriormente selecciona de una lista de usuarios por grupo a todos los integrantes que quiere añadir.

**4.4.3 Requisitos funcionales**  
- Detalles
   - Alcance: Agregar una opción en la interfaz que permita crear un chat grupal. Para cada grupo crear de manera automática una conversación donde participen todos los alumnos y el profesor.
   - Prioridad: Media.
   - Nivel: Alumnos y profesores.
   - Condiciones: Iniciar sesión y pertenecer a un grupo o tener consentimiento de comunicación.
- Consiste en:
   - Un botón que permita crear una conversación grupal.
   - Una lista que contenga a los posibles participantes de la conversación.

- Escenario de éxito:
   - Los usuarios son capaces de crear una sala grupal.
- Escenario de errores:
   - En caso de no contar con conexión a internet se va a guardar las acciones realizadas por el usuario y se va a esperar a la reconexión para efectuarlas.
   - En caso de que el usuario intente dejar la pestaña, se notificará a los usuarios que no se han efectuado las acciones, para que ellos decidan si quieren esperar o abandonar la página.


**5.               Otros requisitos no funcionales**  
**5.1.          Requisitos de rendimiento (Características)**  
- Sistema responsivo: Ya que es un sitio de comunicación, la mayor parte de los usuarios intentan consultar el sitio desde sus dispositivos móviles. Es necesario que el sistema se vea bien en dispositivos móviles para mejorar la experiencia de los alumnos, y puedan utilizar el chat desde su navegador o su dispositivo móvil.
- Sitio Interactivo: La implementación del sitio permite que el usuario interactúe sin la necesidad de cargar la página de nuevo (en particular después de cada submit), creando una experiencia fluida.
- Sistema con protocolos de concurrencia: al ser un sitio de comunicación entre alumnos es muy importante considerar el uso continuo y simultáneo de todos los usuarios, siempre considerando la velocidad de recepción de los mensajes.

**5.2.          Requisitos de seguridad**  
- Inicio de sesión SSO. Al ser un sistema de comunicación donde se maneje información importante o de relevancia para los estudiantes y administrativos se debe asegurar la integridad de los datos e información que ahí se encuentren.
- No cargar datos innecesarios. Al usar solo la información necesaria (sin sacrificar una experiencia placentera del usuario), aseguramos que no habrá pérdida ni abuso de información.
- Usar certificado del sitio para que los datos naveguen de manera segura (SSL)
- Los chats son cifrados y solamente son accesibles para los usuarios involucrados y la institución en caso necesario.

**5.3.          Requisitos de seguridad de la plataforma**  
Los usuarios están comprometidos a:
- No compartir su cuenta con ninguna otra persona.
- Limitarse a un uso adecuado de la información contenida en el sitio, esto es, solo con el fin de comunicarse con la comunidad estudiantil, para fines académicos y de convivencia institucional.  

**5.4.          Atributos de calidad de software**
- Confidencialidad: Se implementan distintas políticas para asegurar la información de los usuarios y el instituto: Solo se usa la información necesaria (Teniendo un buen balance con la experiencia de usuario), y; Se encripta la información al enviarla al navegador y al mandar peticiones a nuestros servidores.
- Integridad: Los datos son correctos y confiables. Toda la información consultada por el alumno proviene únicamente del ITAM. Por otra parte, se implementan protocolos de concurrencia.  
- Disponibilidad: Ya que es un sistema de comunicación para usuarios de la institución se considera un tiempo de disponibilidad del 99 % teniendo considerado un servidor en paralelo para entrar en caso de caída del sistema principal de esta forma evitar grandes tiempos de falta de operación.
- Autenticación: Validamos la identidad de los usuarios a través del sistema de autenticación del ITAM, por lo que no generamos vulnerabilidades adicionales, ni almacenamos información sensible de los usuarios.
- Autorización: Cada alumno solo tiene permiso de consultar y modificar información asociada a su cuenta. Manteniendo siempre solamente los permisos de su tipo de usuario. No tiene medios para alterar datos que no sean suyos.
- Rendición de cuentas: Se lleva registro de todas las actividades realizadas por todos los usuarios, e historial de todas las comunicaciones llevando un log con timestamp para esclarecer cualquier problema.  

**5.5.          Reglas de negocios**  
- Un alumno debe estar inscrito en el ITAM para poder ingresar, el personal docente y administrativo debe trabajar en la institución.   
- Una vez que el alumno deja de estudiar en el ITAM su cuenta es deshabilitada.  
- Los chats que se hagan dentro de la aplicación pueden ser utilizados por el ITAM en caso de ser necesario en cuestiones administrativas, como denuncias de acoso, o casos de deshonestidad académica.




