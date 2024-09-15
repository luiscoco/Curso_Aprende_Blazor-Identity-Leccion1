# CURSO: APRENDE BLAZOR (Identity)

# LECCIÓN 1: Introducción a la Autenticación y Autorización con Blazor

1. Ejecutar Visual Studio 2022 para crear una nueva aplicación con la plantilla Blazor Web App.

2. Elegir la opción de "Authentication de campo: Cuentas individuales"

3. Instalar y ejecutar Docker Desktop

4. Bajar y ejecutar un contenedor docker de SQL Server 2022. Ejecutar la línea de comandos:

```
docker run ^  -e "ACCEPT_EULA=Y" ^  -e "MSSQL_SA_PASSWORD=Luiscoco123456" ^  -p 1433:1433 ^  -d mcr.microsoft.com/mssql/server:2022-latest
```

5. Instalar y ejecutar SQL Server Management Studio 2022 (SSMS)

Server type: Database Engine
Server name: localhost,1433
Authentication: SQL Server Authentication
Login: sa
Password: Luiscoco123456

En SSMS crear la base de datos con este SQL Query:

```
CREATE DATABASE [aspnet-LeccionAuthentication-786afbd3-4fd2-48bc-870d-29133ccc59c8];
GO
```

6. Modificar la cadena de conexión a la base de datos en la aplicación:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost,1433;Database=aspnet-LeccionAuthentication-786afbd3-4fd2-48bc-870d-29133ccc59c8;User Id=sa;Password=Luiscoco123456;Trusted_Connection=False;MultipleActiveResultSets=true;TrustServerCertificate=True"
}
```

7. Crear las tablas e índices en la base de datos de Autenticación y Autorización ejecutando la migración en la aplicación con el comando: Update-Database

8. Ejecutar la aplicación y Registrar un nuevo usuario

9. Acceder a la aplicación con el nombre del usuario creado anteriormente y su contraseña

10. Mostrar la información personal del nuevo usuario 

11. Salir de la cuenta del usuario
