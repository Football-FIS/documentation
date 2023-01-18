# Footmatch

## Introducción
Es una aplicación web que permite a los usuarios ver el estado en tiempo real de los partidos de fútbol de sus equipos favoritos. Con esta herramienta, los usuarios pueden obtener información en tiempo real sobre marcadores, lesiones, inicio/fin del contrato...
  

## Metodología
A continuación, se van a indicar los pasos realizados para la elaboración de este proyecto:


 1.  **Mockup**
Se trata de un prototipo de interfaz de usuario basado en UX (User eXperience) en el que se definirá las funcionalidades y el alcance de la aplicación. Este fichero se llama "*Mockup v3.pdf*" y está añadido en este repositorio.
*Nota: este no representará el diseño final, simplemente sirve como referencia y para concretar los requisitos lo antes posible.*

**Página principal**
![Página principal](images/mock1.png)

**Visualizar partido**
![Visualizar partido](images/mock2.png)

**Login**
![Login](images/mock3.png)

**Ver perfil**
![Ver perfil](images/mock4.png)

**Editar estados del partido**
![Editar estados del partido](images/mock5.png)

 2. **Diagrama de clases**
Se diseñará la estructura de microservicios en función con el análisis previo en el mockup. Para ello se usará un diagrama de clases UML, permitiendo representar así las entidades, relaciones y sus propiedades. Para simplificar la construcción de microservicios, se ha decidido optar por asociar un microservicio a cada entidad, y esta a su vez a una pareja.

*Nota: este no representará el diseño final, simplemente sirve como referencia y para concretar las entidades lo antes posible.*

![UML](images/footmatch-uml-v4.png)


 3. **Desarrollo**
En esta etapa se ha desarrollado los microservicios comenzando por el backend y terminando por el frontend.

4. **Documentación**
Se realiza la documentación asociada a los microservicios, documentación general, revisión de documentación previa en *Customer Agreements*, diapositivas y vídeo de demostración.

## Microservicios
A continuación, se explicará brevemente cada uno de los microservicios que compone la aplicación. Se indicará el enlace con la documentación y el enlace de SwaggerUI (documentación específica de la API).

![Microservices](images/MS.png)

### Team
Representa la entidad que gestiona los equipos. Estos permiten realizar operaciones sobre los jugadores, partidos y los estados. Integra la autenticación y autorización en función del plan dado. 
 - **Documentación**: https://github.com/Football-FIS/team-service
 - **API Rest**: https://team-service-danaremar.cloud.okteto.net/api/v1/docs/

### Player
Representa la entidad que gestiona los jugadores. Además, permitirá el envío de correos electrónicos informativos del partido a los jugadores a modo de recordatorio.
 - **Documentación**: https://github.com/Football-FIS/player-service
 - **API Rest**:

### Match
Representa la entidad que gestiona los partidos asociados a un equipo. Permite entre otras cosas la inicialización del envío de correos a los jugadores.
 - **Documentación**: https://github.com/Football-FIS/match-service
 - **API Rest**: https://match-service-danaremar.cloud.okteto.net/api/v1/docs/

### Match status
Representa el estado en el que se encuentra un partido. Este tipo de estados podrá ser tanto goles, inicio/finalización, tarjetas amarilla/roja, cambio de jugador u otros.
 - **Documentación**: https://github.com/Football-FIS/match-status-service
 - **API Rest**: https://match-status-service-danaremar.cloud.okteto.net/api/v1/docs/


## Términos y condiciones de Footmatch

### Introducción

Le rogamos que lea detenidamente las presentes Condiciones de Uso, ya que rigen el uso que usted haga de los servicios y contenidos proporcionados por Footmatch. Así mismo, al darse de alta en el servicio, aceptará los presentes términos y condiciones.

Para poder utilizar el servicio de Footmatch se requiere tener una edad mínima de 13 años (o la edad mínima equivalente en su país de origen) o contar con el consentimiento de sus padres o tutores legales.

### Duración del contrato
* Se garantiza un periodo mínimo de contrato de 2 años. Tras este periodo, podrán cambiarse las términos y condiciones siempre y cuando se avise al usuario.
* Si se cancela la subscripción, se podrá usar hasta su fecha de finalización.

### Licencia

Todo el software y/o servicios proporcionados son propiedad de Footmatch S.L. y queda totalmente restringido su uso por terceros y distribución.

### Servicio

#### Limitaciones

* Podrá interrumpirse la conexión en caso de que se detecte un uso fraudulento (suplantación de identidad, denegación de servicios...).
* Solamente se podrá aplicar la compra de un futuro plan.
 
#### Disponibilidad

Solamente se garantizará operatividad a los planes de pago, incluyendo las siguientes características:
* Premium: se garantizará una tasa de acierto de 95 cada 100 peticiones realizadas como promedio a lo largo de un mes.
* Enterprise: se garantizará una tasa de acierto de 99 cada 100 peticiones realizadas como promedio a lo largo de un mes.
En caso de incumplimiento, se abonará el siguiente mes de facturación.

### Modalidad de pago

Los pagos deberán realizarse mediante domiciliación bancaria, bajo un previo acuerdo mediante email en el que se indiquen los siguientes datos:
* Nombre y apellidos
* Plan de subscripción
* IBAN

### Pricing

Se ha decidido enfocar un modelo de pricing basado en SaaS, en el que las suscripciones son diferenciadas fundamentalmente por la funcionalidad.
 
No existirán periodos de prueba en los planes de pago.

| Características       | Free   |	Premium | Enterprise    |
|-----------------------|--------|----------|---------------|
| Precio                | Gratis | 5€/mes*  | 25€/mes *     |
| Jugadores máximos     | 16     | 25       | 50 jugadores  |
| Partidos / mes        | 2      | 4        | 10 partidos   |
| Peticiones API / seg  | 5      | 10       | 50            |
| Notificación Email    | NO     | SI       | SI            |
| Predicción del tiempo | NO     | NO       | SI            |
| SLA	                | NO     | NO       | SI            |
* Precio sin impuestos (dependerá del país de origen)

### Soporte

Se garantizará soporte a los planes de pago. Para ver más detalles consultar la siguiente tabla:
 
#### Características

| Características       | Free   |	Premium | Enterprise       |
|-----------------------|--------|----------|------------------|
| Tipo de contacto      | N/A    | email    | sms/email        |
| Tiempo de respuesta   | N/A    | 3 días   | 1 días           |
 
En caso de incumplimiento, se abonará el siguiente mes de facturación.

#### Problemas y disputas

Podrá suspenderse el acceso al servicio Footmatch en cualquier momento si consideramos que ha incumplido las condiciones del servicio, avisando previamente al usuario mediante su correo electrónico.

#### Contacto

Podrá ponerse en contacto mediante:
* Email: footmatch@gmail.com
* Teléfono: +34 666 777 888

### Cambios

Se podrán establecer cambios en el precio o en los términos / condiciones del servicio, siempre y cuando se envié un correo electrónico indicando los cambios y estos sean publicados.

## Análisis de capacidad

## Determinar coste por plan

## Cómputo de horas

## Conclusiones

