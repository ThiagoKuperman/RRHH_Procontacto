#EJERCICIO 2
### 1. ¿Qué es un servidor HTTP?
Un servidor http es un software o sistema que acepta y procesa solicitudes http (hypertext transfer protocol) enviadas por clientes (normalmente navegadores web o aplicaciones) y devuelve respuestas, generalmente en forma de páginas web, archivos o datos estructurados (como json o xml). El servidor http actúa como intermediario entre el cliente y los recursos que se encuentran en un servidor, como archivos, bases de datos o aplicaciones.

El proceso básico de funcionamiento es el siguiente:

El cliente (por ejemplo, un navegador) envía una solicitud http al servidor.
el servidor http recibe la solicitud, la procesa y accede a los recursos necesarios (por ejemplo, archivos html, imágenes o datos de una base de datos).
El servidor devuelve una respuesta http, que puede incluir el contenido solicitado o mensajes de error si no se puede procesar la solicitud correctamente.
Ejemplos de servidores http incluyen apache, nginx, microsoft iis y servidores embebidos en lenguajes de programación como node.js.

### 2. ¿Qué son los verbos HTTP?
Los verbos HTTP, también conocidos como métodos HTTP, son las acciones que un cliente solicita al servidor realizar sobre un recurso determinado. Representan el tipo de operación que el cliente quiere llevar a cabo. Los verbos HTTP más conocidos y utilizados son:

###### GET:
Solicita un recurso o información específica al servidor.
No modifica los datos en el servidor, por lo que es considerado idempotente (múltiples solicitudes iguales tienen el mismo resultado).
Ejemplo: obtener una página web o datos de una API.
###### POST:
Envía datos al servidor para crear o modificar un recurso.
Se utiliza comúnmente en formularios de envío de datos o para enviar información a una API.
No es idempotente, lo que significa que múltiples solicitudes pueden crear múltiples instancias del recurso.
###### PUT:
Envía datos al servidor para reemplazar completamente un recurso existente o para crear uno si no existe.
Es idempotente, lo que significa que realizar la misma solicitud varias veces produce el mismo resultado.
###### PATCH:
Similar a PUT, pero en lugar de reemplazar todo el recurso, solo modifica o actualiza partes del mismo.
No es necesariamente idempotente.
###### DELETE:
Solicita la eliminación de un recurso en el servidor.
Es idempotente; si el recurso ya fue eliminado, las solicitudes sucesivas no tendrán efecto adicional.
###### HEAD:
Similar a GET, pero la respuesta del servidor solo incluye los encabezados de la respuesta, no el cuerpo.
Se utiliza para verificar la existencia de un recurso o para obtener metadatos del mismo sin descargar su contenido.

### 3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?
###### Request:
 Es una solicitud que envía el cliente al servidor, pidiendo un recurso o una acción.
###### Response:
Es la respuesta del servidor al cliente, indicando el resultado de la solicitud.
Headers: Son metadatos que acompañan el request y el response, proporcionando información adicional (como tipo de contenido, autenticación, etc.).
### 4. ¿Qué es un queryString? (En el contexto de una URL)
Es una cadena de parámetros que se añade a la URL después del símbolo ? para enviar datos al servidor. Ejemplo: ?nombre=Juan&edad=25.

### 5. ¿Qué es el responseCode? ¿Qué significado tienen los posibles valores devueltos?
El responseCode es un código de estado que indica el resultado de una solicitud HTTP:

200 OK: Éxito.
404 Not Found: Recurso no encontrado.
500 Internal Server Error: Error del servidor.
### 6. ¿Cómo se envía la data en un GET y cómo en un POST?
###### GET:
La data se envía en la URL como parte del query string.
###### POST: 
La data se envía en el cuerpo de la solicitud.
### 7. ¿Qué verbo HTTP utiliza el navegador cuando accedemos a una página?
El navegador usa el verbo GET.

### 8. ¿Qué son las estructuras de datos JSON y XML?
###### JSON: 
Un formato de texto ligero para representar datos, basado en pares clave-valor. Ejemplo:

```json
{
  "nombre": "Thiago",
  "edad": 21
}
```
**XML**: Un lenguaje de marcado utilizado para estructurar datos con etiquetas. Ejemplo:
```xml
<persona>
  <nombre>Thiago</nombre>
  <edad>21</edad>
</persona>
```
### 9. ¿Qué es el estándar SOAP?
**SOAP** (Simple Object Access Protocol) es un protocolo de comunicación que utiliza XML para enviar mensajes estructurados entre aplicaciones web, comúnmente usado en servicios web.

### 10. ¿Qué es el estándar RESTful?
REST (Representational State Transfer) es un estilo arquitectónico que define cómo las aplicaciones web se comunican utilizando recursos y verbos **HTTP** como **GET, POST, PUT, y DELETE**. Es simple y ligero comparado con **SOAP.**

### 11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Headers en un request: Son metadatos que proporcionan información sobre la solicitud (tipo de contenido, autenticación, etc.).
Content-Type: Especifica el tipo de contenido del cuerpo del request o response (por ejemplo, application/json para datos en formato JSON)

# EJERCICIO 3

###  1.	Realizar un request GET a la URL

 ![IMAGEN GET](/Tp_kuperman/img/GET1.jpeg)


### 2.	Realizar un request POST a la URL anterior

![Texto alternativo](/Tp_kuperman/img/POST.jpeg)


### 3. Realizar nuevamente un request GET a la URL

![IMAGEN GET](/Tp_kuperman/img/GET2.jpeg)

# EJERCICIO 4

### compartir la URL del perfil público de Trailhead 

[https://www.salesforce.com/trailblazer/tkuperman](https://www.salesforce.com/trailblazer/tkuperman "https://www.salesforce.com/trailblazer/tkuperman")

# EJERCICIO 5

**1.Lead**
 -Concepto: Un Lead representa a una persona o empresa potencialmente interesada en los productos o servicios. Es un registro sin cualificar que aún no se ha convertido en una oportunidad o cuenta.
 -Datos almacenados: Nombre, empresa, correo electrónico, número de teléfono, fuente de generación, etc.
 -Relaciones: Puede convertirse en un Account, Contact y Opportunity.
**2. Account**
-Concepto: Un Account representa una empresa o entidad con la que se tiene una relación de negocio. Es el cliente formal o potencial.
-Datos almacenados: Nombre de la cuenta, dirección, número de teléfono, tipo de industria, tamaño de la empresa, etc.
-Relaciones: Se relaciona con Contact (personas asociadas a la cuenta), Opportunity (posibles ventas), Asset (productos que tiene el cliente), y Case (consultas o problemas del cliente).
**3. Contact**
-Concepto: Un Contact representa a una persona dentro de una empresa (Account) con la que se mantiene comunicación o negocio.
-Datos almacenados: Nombre, cargo, teléfono, correo electrónico, dirección, cuenta relacionada.
-Relaciones: Se asocia principalmente a un Account, puede estar vinculado a Opportunity y Case.
**4. Opportunity**
-Concepto: Una Opportunity representa una posible venta o trato con un cliente. Es parte del proceso de ventas.
-Datos almacenados: Valor de la oportunidad, fecha de cierre, etapa de ventas, cuenta relacionada, productos asociados.
-Relaciones: Se relaciona con Account, Product, Quote y PriceBook. Puede incluir Contact como persona involucrada en la oportunidad.
**5. Product**
-Concepto: Un Product es un artículo o servicio que una empresa vende a sus clientes.
-Datos almacenados: Nombre del producto, descripción, precio, código de producto.
-Relaciones: Se relaciona con PriceBook (para definir precios específicos) y Opportunity (para asociar productos a oportunidades de venta).
**6. PriceBook**
-Concepto: Un PriceBook es una lista de productos y sus precios asociados. Se utiliza para ofrecer precios estándar o específicos a los clientes.
-Datos almacenados: Lista de productos y precios.
-Relaciones: Se relaciona con Product, Opportunity y Quote para definir el precio de los productos.
**7. Quote**
-Concepto: Un Quote es una oferta formal enviada al cliente que detalla los productos o servicios y los precios ofrecidos.
-Datos almacenados: Detalles de la oportunidad, productos y precios, fecha de emisión, descuento.
-Relaciones: Se relaciona con Opportunity, Product y PriceBook.
**8. Asset**
-Concepto: Un Asset representa los productos o servicios que un cliente ha comprado y tiene en su posesión.
-Datos almacenados: Nombre del producto, cuenta relacionada, fecha de compra, número de serie, estado.
-Relaciones: Se asocia con Account y puede estar vinculado a Case (si hay problemas o solicitudes de soporte).
**9. Case**
-Concepto: Un Case es una solicitud de soporte o problema que un cliente tiene con un producto o servicio.
-Datos almacenados: Detalles del problema, estado, prioridad, cuenta o contacto relacionado, activos asociados.
-Relaciones: Se relaciona con Account, Contact, Asset y puede estar vinculado a Article (como base de conocimiento).
**10. Article**
-Concepto: Un Article es una pieza de contenido en la base de conocimiento que proporciona soluciones o información a los problemas comunes de los clientes.
-Datos almacenados: Título, contenido, categoría, fecha de publicación.
-Relaciones: Puede estar relacionado con Case para ofrecer soluciones documentadas a problemas recurrentes.

### Diagrama:

![IMAGEN GET](/Tp_kuperman/img/Salesforce.drawio.png)


# EJERCICIO 6

### Soluciones de Salesforce
###### A. ¿Qué es Salesforce?
Salesforce es una plataforma de gestión de relaciones con clientes (CRM) basada en la nube que permite a las empresas gestionar ventas, marketing, servicio al cliente y otras operaciones comerciales.

###### B. ¿Qué es Sales Cloud?
Sales Cloud es una solución de Salesforce diseñada para ayudar a las empresas a gestionar el ciclo completo de ventas, desde leads hasta oportunidades y clientes.

###### C. ¿Qué es Service Cloud?
Service Cloud es una solución de Salesforce enfocada en el servicio al cliente, que permite gestionar casos, ofrecer soporte y automatizar servicios a través de múltiples canales.

###### D. ¿Qué es Health Cloud?
Health Cloud es una solución de Salesforce orientada al sector de la salud, que permite gestionar relaciones y datos de pacientes de manera segura y personalizada.

###### E. ¿Qué es Marketing Cloud?
Marketing Cloud es una plataforma de Salesforce para gestionar y automatizar campañas de marketing, desde correos electrónicos y redes sociales hasta la personalización de la experiencia del cliente.

### Funcionalidades de Salesforce
###### A. ¿Qué es un RecordType?
Un RecordType permite crear diferentes tipos de registros dentro de un mismo objeto, ofreciendo diferentes layouts, procesos de negocio y valores predeterminados.

###### B. ¿Qué es un ReportType?
Un ReportType define la estructura de los informes, indicando qué objetos y campos pueden ser utilizados para generar reportes.

###### C. ¿Qué es un Page Layout?
Un Page Layout es la disposición de los campos, botones y enlaces en la interfaz de usuario de un registro de Salesforce.

###### D. ¿Qué es un Compact Layout?
Un Compact Layout muestra un conjunto mínimo de campos importantes cuando se ve un registro en la vista móvil o en la vista previa del escritorio.

###### E. ¿Qué es un Perfil?
Un Perfil en Salesforce define los permisos de acceso y las configuraciones disponibles para los usuarios, controlando qué pueden ver y hacer en la plataforma.

###### F. ¿Qué es un Rol?
Un Rol es una jerarquía que determina el acceso a los registros basados en la estructura organizacional, permitiendo el control del acceso a los datos.

###### G. ¿Qué es un Validation Rule?
Una Validation Rule asegura que los datos ingresados en un registro cumplan con ciertos criterios, evitando errores o inconsistencias.

###### H. ¿Qué diferencia hay entre una relación Master-Detail y Lookup?

Master-Detail: Relación fuerte donde el registro hijo depende del padre. Si el padre se elimina, el hijo también.
Lookup: Relación más flexible, donde los registros pueden existir independientemente uno del otro.
###### I. ¿Qué es un Sandbox?
Un Sandbox es un entorno de prueba en Salesforce que replica la configuración y datos del entorno de producción, permitiendo probar cambios sin afectar la operación real.

###### J. ¿Qué es un ChangeSet?
Un ChangeSet es un conjunto de configuraciones y componentes personalizados que pueden ser transferidos de un entorno de Salesforce a otro, por ejemplo, de un Sandbox a producción.

###### K. ¿Para qué sirve el import Wizard de Salesforce?
El Import Wizard permite importar datos a Salesforce de forma sencilla para objetos estándar como leads, contactos, cuentas y otros.

###### L. ¿Para qué sirve la funcionalidad Web to Lead?
Web to Lead permite capturar datos de clientes potenciales (leads) a través de un formulario web y enviarlos directamente a Salesforce.

###### M. ¿Para qué sirve la funcionalidad Web to Case?
Web to Case permite capturar solicitudes de servicio al cliente desde un formulario web y crear automáticamente casos en Salesforce.

###### N. ¿Para qué sirve la funcionalidad Omnichannel?
Omnichannel distribuye automáticamente el trabajo entrante (como casos o leads) a los agentes disponibles en función de su capacidad, asegurando una distribución equilibrada.

###### O. ¿Para qué sirve la funcionalidad Chatter?
Chatter es una herramienta de colaboración dentro de Salesforce que permite a los usuarios compartir información, documentos y comunicarse en tiempo real.

### Conceptos generales
###### A. ¿Qué significa SaaS?
SaaS (Software as a Service) es un modelo de distribución de software donde las aplicaciones se alojan en la nube y se accede a ellas a través de internet.

###### B. ¿Salesforce es SaaS?
Sí, Salesforce es una plataforma SaaS.

###### C. ¿Qué significa que una solución sea Cloud?
Una solución en la nube se accede y almacena en servidores remotos a través de internet, en lugar de estar instalada localmente.

###### D. ¿Qué significa que una solución sea On-Premise?
Una solución On-Premise está instalada y gestionada localmente en los servidores de la empresa, en lugar de estar en la nube.

###### E. ¿Qué es un pipeline de ventas?
Un pipeline de ventas es una representación visual del proceso de ventas, mostrando en qué etapa se encuentran las oportunidades y su probabilidad de cierre.

###### F. ¿Qué es un funnel de ventas?
Un funnel de ventas es un modelo que describe el viaje de los clientes potenciales desde la etapa de descubrimiento hasta la conversión en clientes.

###### G. ¿Qué significa Customer Experience?
Customer Experience (CX) es la percepción total que un cliente tiene sobre su interacción con una empresa, desde el primer contacto hasta el servicio postventa.

###### H. ¿Qué significa omnicanalidad?
Omnicanalidad es la capacidad de ofrecer una experiencia de cliente fluida y coherente a través de múltiples canales de comunicación (web, móvil, tienda física, etc.).

###### I. ¿Qué significa que un negocio sea B2B? ¿Qué significa que un negocio sea B2C? ¿Qué es un KPI?

B2B: Business to Business, negocios que venden a otras empresas.
B2C: Business to Consumer, negocios que venden directamente al consumidor.
KPI: Key Performance Indicator, un indicador clave de rendimiento que mide el éxito de un proceso o actividad.
###### J. ¿Qué es una API y en qué se diferencia de una Rest API?

API: Es una interfaz que permite la comunicación entre diferentes aplicaciones o sistemas.
REST API: Es un tipo de API que sigue los principios de arquitectura REST, usando HTTP y operaciones como GET, POST, PUT, DELETE.
###### K. ¿Qué es un Proceso Batch?
Un proceso batch es un tipo de procesamiento en el que las operaciones se agrupan y se ejecutan en lote, generalmente para manejar grandes volúmenes de datos.

###### L. ¿Qué es Kanban?
Kanban es un método de gestión visual de tareas que ayuda a controlar el flujo de trabajo, utilizando tarjetas o columnas para representar tareas en diferentes etapas.

###### M. ¿Qué es un ERP?
ERP (Enterprise Resource Planning) es un sistema integrado que gestiona y automatiza las principales actividades empresariales como contabilidad, inventario, ventas, y más.

###### N. ¿Salesforce es un ERP?
No, Salesforce es un CRM, aunque tiene funcionalidades avanzadas que pueden integrarse con ERP.


# EJERCICIO 6
### Ejercicio A
```
public class JsonHttpClient {
    // Método estático para realizar una solicitud GET
    public static void getJsonData() {
        // URL del archivo JSON
        String url = 'https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json';
        // Crear una solicitud HTTP
        Http http = new Http();
        HttpRequest request = new HttpRequest();
        request.setEndpoint(url);
        request.setMethod('GET');


        // Realizar la solicitud
        HttpResponse response;
        try {
            response = http.send(request);
            // Verificar el estado de la respuesta
            if (response.getStatusCode() == 200) {
                // Procesar los datos JSON
                String jsonData = response.getBody();
                System.debug('Datos JSON: ' + jsonData);
               
                // Deserializar el JSON en un Map
                Map<String, Contact> contacts = (Map<String, Contact>) JSON.deserialize(jsonData, Map<String, Contact>.class);
               
                // Procesar los datos deserializados
                for (String key : contacts.keySet()) {
                    Contact contact = contacts.get(key);
                    System.debug('ID: ' + key + ', Nombre: ' + contact.name + ', Email: ' + contact.email);
                }
            } else {
                System.debug('Error en la respuesta: ' + response.getStatus());
            }
        } catch (Exception e) {
            System.debug('Excepción: ' + e.getMessage());
        }
    }
}
```
######  Lo llamamos en la consola con:
         

    JsonHttpClient.getJsonData();
         
### Ejercicio C



    trigger UpdateContactEmail on Contact (before insert, before update) {
    for (Contact con : Trigger.new) {
            if (con.idprocontacto__c == '-O9Q1yYchGkusWhmJMsM') {
                String url = 'https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts/' + con.idprocontacto__c + '.json';
                Http http = new Http();
                HttpRequest req = new HttpRequest();
                req.setEndpoint(url);
                req.setMethod('GET');
    
    
                HttpResponse res = http.send(req);
                if (res.getStatusCode() == 200) {
                    Map<String, Object> results = (Map<String, Object>) JSON.deserializeUntyped(res.getBody());
                    if (results.containsKey('email')) {
                        con.Email = (String) results.get('email');
                    }
                }
            }
        }
    }
¡
**Table of Contents**

[TOCM]

[TOC]

