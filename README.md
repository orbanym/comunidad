============================================================
             PORTAL DE EVENTOS COMUNITARIOS
============================================================

Instrucciones de Instalación
----------------------------

1. Requisitos Previos:
   - Servidor Web (como Apache o Nginx)
   - PHP 7.4 o superior
   - MySQL 5.7 o superior
   - Herramienta de gestión de bases de datos (phpMyAdmin, MySQL Workbench, etc.)

2. Configuración de la Base de Datos:
   - Crea una base de datos en tu servidor MySQL llamada `comunitaria`.
   - Importa el archivo `comunitaria_database.sql` proporcionado en el directorio raíz del proyecto.
     Este archivo creará las tablas necesarias e insertará datos de ejemplo.
   - Puedes usar la siguiente línea de comando para importar el archivo SQL:
     ```
     mysql -u [usuario] -p [contraseña] comunitaria < /ruta/a/comunitaria_database.sql
     ```
   - O usar la opción "Importar" en herramientas como phpMyAdmin o MySQL Workbench.

3. Configuración del Proyecto:
   - Asegúrate de que el proyecto esté ubicado en el directorio raíz del servidor web (por ejemplo, `/var/www/html/comunitaria` o `C:\xampp\htdocs\comunitaria`).
   - Configura el archivo `db.php` en el directorio `includes` para que apunte a tu base de datos:
     ```php
     <?php
     $servername = "localhost"; // Dirección del servidor MySQL
     $username = "tu_usuario";  // Usuario de la base de datos
     $password = "tu_contraseña"; // Contraseña del usuario
     $dbname = "comunitaria";    // Nombre de la base de datos

     $conn = new mysqli($servername, $username, $password, $dbname);

     if ($conn->connect_error) {
         die("Conexión fallida: " . $conn->connect_error);
     }
     ?>
     ```

4. Estructura de Archivos del Proyecto:
   - `/assets/`: Contiene CSS, imágenes y archivos JavaScript.
   - `/includes/`: Contiene archivos de configuración compartidos como `header.php`, `footer.php` y `db.php`.
   - `/events/`: Contiene páginas relacionadas con los eventos (visualización, CRUD).
   - `/users/`: Contiene páginas de registro, inicio y cierre de sesión.
   - `/admin/`: Contiene páginas para la administración del sistema.

5. Uso del Sistema:
   - Accede al portal desde tu navegador en `http://localhost/comunitaria`.
   - Usa las siguientes credenciales para probar el sistema:
     * **Administrador:**
       - Email: `admin@comunitaria.com`
       - Contraseña: `admin123`
     * **Usuario Regular:**
       - Email: `user@comunitaria.com`
       - Contraseña: `user123`

6. Información Adicional:
   - Asegúrate de tener permisos adecuados para el acceso a archivos en el servidor.
   - Si usas XAMPP, asegúrate de iniciar Apache y MySQL desde el panel de control.

7. Contacto:
   Para cualquier consulta o soporte, puedes ponerte en contacto con el autor.

============================================================
Autor:
Orbany Marine
Correo de Contacto: Orbany.marine@gmail.com
============================================================
