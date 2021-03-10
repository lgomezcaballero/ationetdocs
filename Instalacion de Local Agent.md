![ationetlogo](Content/Images/ATIOnetLogo_250x70.png)

|**Información del Documento**|.|
|--- |--- |
|**Archivo:**|ATIONet-Instalacion-de-Local-Agent.md|
|**Versión del Doc.:**|1.0|
|**Fecha de Publicación:**|10, Marzo 2021|
|**Autor:**|ATIO International LLC|


|**Registro de Cambios**|||
|--- |--- |--- |
|**Ver.**|**Fecha**|**Resumen de Cambios**|
|1.0|10/Mar/2021|- Versión Inicial

## Contenido

- [Herramientas necesarias](#herramientas-necesarias)

# **Guía de instalación de Local Agent**

# **Herramientas necesarias**

- Pendrive
- Teclado
- Mouse
- Monitor

# **Pasos de instalación**

Para la instalación del servicio existen ciertos prerrequisitos. Los prerrequisitos necesarios para instalar Local Agent son los siguientes:

- .Net Framework 4.5
- Sql Express 2008 - Atio Custom Instance
- Windows Installer 3.1
- Windows Installer 4.5

Cada programa se puede descargar directamente de la página oficial de Microsoft, sin embargo, en nuestro [repositorio oficial](https://github.com/Ationet/ationetdownloads/blob/master/README.md) podemos conseguir estos prerrequisitos junto con el instalador de Local Agent, el cual instala todos los programas automáticamente, de una sola vez sin la necesidad de ir instalando un por uno por separado.

Desde el repositorio podrá localizar los siguientes archivos para descargar:

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/ATIONet%20Download%20Center%20Site.png)

Una vez descargado el paquete de archivos, vamos a ver los siguientes ejecutables:

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Paquete%20Archivos.png)

El ejecutable &quot;Setup.exe&quot;, se encarga de ejecutar todos los instaladores con los prerrequisitos. Es importante que los archivos de prerrequisitos estén en la misma carpeta que el ejecutable **Setup.exe** y descomprimidos.

El equipo va chequear si tiene todo instalado, y en caso de no tenerlo el programa de instalación se encargará de agregar todos los prerrequisitos que hagan falta. Una vez llegado el momento de la instalación del Local Agent veremos la siguiente imagen:

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Asistente%20de%20Instalaci%C3%B3n.png)

Haremos click en siguiente, luego de eso nos preguntará la ubicación de donde instalar los datos del servicio, en este caso utilizaremos la default.

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Selecci%C3%B3n%20Carpeta%20de%20Instalaci%C3%B3n.png)

Damos siguiente una vez más y el Local Agent pedirá confirmación nuevamente. Una vez confirmado, el instalador llegará al 75% de la instalación y alcanzado este punto abrirá una ventana emergente con el pedido de un archivo, este mismo es el **install.config**.

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Selecci%C3%B3n%20Install.Config.png)

Una vez encontrado y seleccionado el archivo, la instalación del Local Agent continuará.

Cuando finalice la instalación, haremos click en **Finalizar** para terminar con la instalación del mismo.

## **Como armar el archivo install.config**

El **install.config** es un archivo de texto que se puede editar/crear con bloc de notas. Los datos que deben figurar en el archivo son los siguientes:

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Install.Config.png)

Breve aclaración sobre los apartados del **install.config**:

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Configuraci%C3%B3n%20Install.Config.png)

Para que nuestro equipo se pueda conectar con el portal de Ationet deberemos modificar el **Subscriber_Code**. Para descubrir cuál es el de nuestro sitio deberemos ingresar en el portal de ATIONet, ingresar al apartado **Administración - Terminales / Controladores**.

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Terminales-Controladores.png)

Una vez estemos en este apartado deberemos copiar los primero tres caracteres que se encuentran en el apartado de Código y colocarlos en **Subscriber_Code**.

## **Revisión de logs luego de la instalación**

Una vez finalizada la instalación procedemos a verificar los logs para ver si completó la descarga de datos correspondiente para la base offline.

Los logs se encuentran ubicados por defecto en:

**C:\Program Files (x86)\ATIONet\ATIONet Local Agent\logs**

# **Estadisticas**

La siguiente información compartida es en un ambiente de prueba. Estos son los tiempos de espera de subida de datos del Local Agent cuando pasa de modo OFFLINE a ONLINE.

![](https://github.com/Ationet/ationetdocs/blob/master/Content/Images/Local%20Agent/Estad%C3%ADsticas.png)