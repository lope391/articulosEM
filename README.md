# articulosEM

By: Edwin Montoya Munera - emontoya@eafit.educo

# 1. Descripción de aplicación

Aplicación web que permite gestionar Articulos.

Se generó la base, con Yeoman:

    $ yo express

(este generador, crea una app base ejemplo MVC para gestión de articulos)

Ejemplo de clase, a modo de tutorial, que cubre:

* Aplicación del patron MVC a una aplicación Web
* Uso de un framework backend moderno -> NodeJS
* Configuración de ambientes: Desarrollo, Pruebas y Producción.

# 2. Análisis

## 2.1 Requisitos funcionales:

1. Crear Articulo.
2. Buscar articulo por parte del titulo
3. Borrar articulo por Id de articulo
4. Listar todos los articulos de la base de datos en la página home o index

## 2.2 Definición de tecnología de desarrollo y ejecución para la aplicación:

* Lenguaje de Programación: Javascript
* Framework web backend: NodeJS - Express
* Framework web frontend: no se usa - se utilizará Templates HTML para Vista (V)
* Base de datos: MongoDB
* Web App Server: NodeJS
* Web Server: NGINX

## Ambiente de Desarrollo, Pruebas y Producción:

## Desarrollo:

## Pruebas

en el DCA:

1. se instala nvm local para el usuario

source: https://www.liquidweb.com/kb/how-to-install-nvm-node-version-manager-for-node-js-on-centos-7/

2. se instala la version de node:

    $ nvm install v7.7.4

3. se instala el servidor mongodb

como root:

    # yum install mongodb-server -y

ponerlo a correr:

    # systemctl enable mongod
    # systemctl start mongod


lo instala de los repositorios propios de Centos.

tambien lo puede instalar de un repo de mongodb:

ver pág: https://www.liquidweb.com/kb/how-to-install-mongodb-on-centos-7/




# 3. Diseño:

## 3.1 Modelo de datos:

article:

{
    title: String,
    url: String,
    text: String
}

## 3.2 Servicios Web

    /* Servicio Web: Inserta un registro de Articulo en la Base de datos
      Método: POST
      URI: /newarticle
    */

    /* Servicio Web: Realiza la búsqueda en la base de datos, por campo titulo
      Método: GET
      URI: /findbytitle?title=val
    */

/* Servicio Web: Realiza la búsqueda en la base de datos de todos los articulos
  Método: GET
  URI: /articles
*/

/* Servicio Web: Borra un Articulo de la Base de datos.
  Método: GET
  URI: /delarticle?id=val
 */

 /* Servicio Web: Borra un Articulo de la Base de datos.
   Método: DELETE
   URI: /delarticle/id
  */

# 4. Desarrollo:

# 5. Implementación o Despliegue:

5.1 despliegue en el data center academico:

la primera vez:
