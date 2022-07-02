# express api

Aplicación base para REST API con Node.js y Express.js

API Endpoints

| Methods       | Urls              |  Descripción                 |
| -----------   | ----------------  |  --------------------------  |
| GET           | api/employees     |  Get all employees           |
| GET           | api/employees/id  |  Get a specific employee     |
| POST          | api/employees     |  Create a new employee       |
| PUT           | api/employees/id  |  Update an existing employee |
| DELETE        | api/employees/id  |  Delete an existing employee |

## Quick Start

Clonamos el repositorio

```bash
git clone https://github.com/corevill/basic-express-rest-api.git
```

Entramos dentro de la carpeta del proyecto que hemos clonado

```bash
cd basic-express-rest-api
```

Creamos el fichero.env

```bash
echo "" > .env
```

Abrimos el fichero que hemos creado e incluimos en el la configuración de nuestra aplicación

```
DB_URL = localhost/my-employees
TEST_DB_URL = localhost/test-my-employees
PORT = 5000
```

Instalamos las dependencias

```bash
npm install
```

Arrancamos nuestro servidor

```bash
npm run dev
``` 

## Instalar MongoBD Community Server 

Para que este ejemplo funcione correctamente debemos configurar una BD de MongoDB donde tengamos employee creado.

- Descargar el instalador de la página oficial e instalamos MongoDB de forma completa y nos quedamos con la ruta de instalación

- Creamos en el siguiente directorio C:\data\db

- Luego vamos con consola de Administrador a la carpeta donde instalamos mongo, normalmente "C:\Program Files\MongoDB\Server\5.0\bin" y ejecutamos el comando 
    ```bash
    mongod.exe
    ```

- Con esto tendremos el servidor corriendo. En la consola nos aparecerá la IP y el puerto. Normalmente la IP que nos mostrará será la de la máquina local "localhost" y el puerto 27017

- Con la información anterior abrimos la aplicación MongoDB Compass que instalamos previamente e incluimos la ruta a nuestra bd "localhost:27017"

- Una vez hecho esto ya deberíamos ver el panel de control de MongoDB y crear una BD llamada Employees.

- Con todos estos pasos el fichero .env debería tener la siguiente pinta:
    
    DB_URL = localhost:27017/Employees
    TEST_DB_URL = localhost:27017/Employees
    PORT = 5000

Artículo de origen [Build a Restful CRUD API with Node.js](https://dev.to/zagaris/build-a-restful-crud-api-with-node-js-2334).
