# Proyecto Space (BotIA)

El siguiente documento tiene como propósito de ser una manual de operación para el proyecto denominado como "SpaceBot"

### Introducción

El SpaceBot es un ecosistema diseñado para extraer la información de facturas de los clientes de la empresa SpaceAdudanas. Esta diseñando para leer facturas en formato PDF/A y para extraer la información necesaria de ellas. El SpaceBot toma la información de la factura, la analiza y la organiza para que el usuario pueda usarla de manera fácil y rápida. El SpaceBot también ofrece la opción de exportar la información extraída en un formato compatible con la contabilidad de la empresa. Esto permite a los usuarios ahorrar tiempo y esfuerzo, al eliminar la necesidad de revisar y transcribir manualmente la información de las facturas. Además, el SpaceBot también ofrece herramientas para verificar la información extraída, como la validación de datos, para asegurar que los datos sean exactos.El SpaceBot es un ecosistema diseñado para extraer la información de facturas de los clientes de la empresa SpaceAdudanas. Esta diseñando ;para leer facturas en formato PDF/A y para extraer la información necesaria de ellas. El SpaceBot toma la información de la factura, la analiza y la organiza para que el usuario pueda usarla de manera fácil y rápida. El SpaceBot también ofrece la opción de exportar la información extraída en un formato compatible con la contabilidad de la empresa. Esto permite a los usuarios ahorrar tiempo y esfuerzo, al eliminar la necesidad de revisar y transcribir manualmente la información de las facturas. Además, el SpaceBot también ofrece herramientas para verificar la información extraída, como la validación de datos, para asegurar que los datos sean exactos.

## Tecnologías

* Python

* Herramientas de lenguaje natural 

* SQL-Server 

* Fast-API

* Py-Tabula

### Funcionamiento

El funcionamiento de spacebot consiste en 4 modulos los cuales son independientes entre si, los cuales no estan adaptados para acada una de las empresas asociadas al cliente.

La suluciones propuestas se dividen en 2 la cuales se le donominan como empresas con template y empresas sin el mismo. la cual cada una cuenta con el entorno de desarrollo personalizado para cada una de ellas, esto para que cada una de las empresas asociadas al cliente pueda generar las soluciones deseadas.

![MarineGEO circle logo](assets\BotSpace%20Program.drawio%20(1).png)

#### Empresas con Template

Las empresas con template, son aquellas empresas que cuentan con un template predefinido, el cual se le aplica al momento de leer la factura. El SpaceBot lee la información de la factura con el template y genera una salida en formato JSON con los datos necesarios. Esto permite al usuario tener una salida lista para su procesamiento. Esta opción es útil cuando las facturas son similares, ya que el template guarda los datos en el mismo orden para cada factura. 

#### Empresas sin Template

 Las empresas sin template, son aquellas empresas que no cuentan con un template predefinido. En esta opción, el SpaceBot toma la información de la factura y la procesa con tecnología de lenguaje natural para generar una salida en formato JSON con los datos necesarios. Esta opción es útil cuando las facturas son diferentes, ya que el SpaceBot detecta los datos en cada factura de manera independiente.

### Base de datos

![](assets\2022-12-16-09-46-08-Diagrama.png)

La base de datos parece contener las siguientes tablas y campos:

1. clients
   
   - RFC_clients (nvarchar(50))
   - Name_clients (nvarchar(max))

2. invoices
   
   - Num_invoices (bigint)
   - Date_invoices (date)
   - Origin_invoices (varchar(500))
   - Total_invoices (float)
   - RFC_clients (nvarchar(50))

3. items
   
   - Id_items (int)
   - Description_items (nvarchar(50))
   - Quantity_items (float)
   - Mesure_items (nvarchar(50))
   - Cost_items (float)
   - Num_invoice (bigint)

4. pdfs
   
   - id_pdfs (int)
   - author_pdfs (varchar(max))
   - path_pdfs (varchar(max))
   - status_pdfs (varchar(50))

5. provedores
   
   - id_fiscal (int)
   - name (varchar(max))
   - ident_fiscal (varchar(max))

6. users
   
   - email_users (nvarchar(50))
   - password_users (nvarchar(max))
   - isadmin_users (bit)
   - username_users (nvarchar(50))

Además, se han definido varias relaciones de clave externa:

1. dbo.clients.RFC_clients es una clave externa que se refiere a dbo.invoices.RFC_clients
2. dbo.invoices.Num_invoices es una clave externa que se refiere a dbo.items.Num_invoice
3. dbo.users.email_users es una clave externa que se refiere a dbo.pdfs.author_pdfs

### Requisitos

Para poder usar el SpaceBot, es necesario tener una computadora con los siguientes requisitos: 

- Procesador Intel Core i7 o superior

- 8 GB de RAM 

- Sistema operativo Windows 10 

- Almacenamiento de 500 GB 

- Una conexión a Internet

[Instalacion](install.md)

[Instruciones de uso](manual.md)

[Fallas comunes](fix.md)
