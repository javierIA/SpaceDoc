# Instalación(BOT)

Para clonar un repositorio de Git, primero debes tener Git instalado en tu sistema. Una vez que esté instalado, puedes clonar un repositorio usando el comando `git clone`, seguido del URL del repositorio que deseas clonar. Por ejemplo:

```bash
git clone https://github.com/user/repo.git`
```

Reemplaza `username` y `repository` con el nombre de usuario y el nombre del repositorio de SpaceBot en Github, respectivamente. Luego, entra en el directorio que se creó al clonar el repositorio:

```bash
 cd repository
```

Una vez en el directorio, puedes instalar las dependencias necesarias para ejecutar SpaceBot con el administrador de paquetes de Python, pip. Ejecuta el siguiente comando:

```bash
pip install -r requirements.txt
```

Este comando instalará todas las dependencias necesarias para ejecutar SpaceBot. Una vez que se completa la instalación, puedes iniciar SpaceBot ejecutando el siguiente comando:

```bash
python app.py
```

Esto iniciará SpaceBot y lo pondrá a correr en tu ordenador y iniciara con la extracion de los documentos en tabla

# Base de datos

Para instalar la base de datos de SQL Server de SpaceBot desde un archivo `base.sql`, primero debes descargar e instalar SQL Server en tu sistema. Puedes descargar SQL Server desde el sitio web de Microsoft. Una vez que hayas instalado SQL Server, debes crear una base de datos vacía para SpaceBot. Puedes hacerlo ejecutando el siguiente comando en la consola de SQL Server:

```sql
CREATE DATABASE spacebot;
```

En el directorio del repositorio, busca el archivo `base.sql` y cópialo a una ubicación en tu sistema donde puedas acceder a él fácilmente. Luego, abre la consola de SQL Server y conéctate a la base de datos que creaste anteriormente:

```sql
USE spacebot;
```

Reemplaza `spacebot` con el nombre que le diste a la base de datos. Una vez que estés conectado a la base de datos, puedes importar el contenido del archivo `base.sql` ejecutando el siguiente comando:

```sql
SOURCE path/to/base.sql;
```

Reemplaza `path/to/base.sql` con la ruta al archivo `base.sql` en tu sistema. Este comando importará el contenido del archivo en la base de datos. Asegúrate de tener una conexión a Internet activa para que la importación se complete correctamente. Una vez que se complete la importación, puedes iniciar SpaceBot ejecutando el siguiente comando:

# Instalación(WEB)

Para descargar y instalar un proyecto de SpaceBot web de github en un servidor de Windows, sigue estos pasos:

1. Abre una consola de comandos en tu servidor Windows y dirígete a la carpeta donde quieres instalar el proyecto.

2. Clona el proyecto de FastAPI de github utilizando el comando `git clone https://github.com/[usuario]/[proyecto].git`, reemplazando [usuario] y [proyecto] con el usuario y el nombre del proyecto de FastAPI en github.

3. Una vez que el proyecto se haya clonado en tu servidor, dirígete a la carpeta del proyecto utilizando el comando `cd [proyecto]`.

4. Asegúrate de tener Python 3.6 o superior instalado en tu servidor Windows y crea un entorno virtual para el proyecto utilizando el comando `python -m venv env`.

5. Activa el entorno virtual utilizando el comando `env\Scripts\activate.bat` en Windows o `source env/bin/activate` en Linux o Mac.

6. Instala las dependencias del proyecto utilizando el comando `pip install -r requirements.txt`.

7. Una vez que las dependencias se hayan instalado, inicia el proyecto utilizando el comando `uvicorn main:app --reload`.

8. Abre tu navegador y ve a la dirección [http://localhost:8000](http://localhost:8000/) para verificar que el proyecto de FastAPI se haya instalado correctamente en tu servidor Windows.

Algunos de los posibles errores al descargar y instalar un proyecto de FastAPI en un servidor Windows son:

- No tener Python 3.6 o superior instalado en el servidor.
- No tener git instalado en el servidor.
- No tener acceso a internet para clonar el proyecto de github.
- No tener permisos de escritura en la carpeta donde se quiere instalar el proyecto.
- No tener las dependencias necesarias instaladas en el entorno virtual del proyecto.
- Problemas con el archivo requirements.txt o con la instalación de las dependencias.
- Problemas con el archivo de configuración del proyecto o con el inicio del mismo.
- Conflictos de puertos en el servidor, lo que impediría que el proyecto se inicie correctamente.
