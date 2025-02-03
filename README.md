
# Guía Técnica para Clonar y Ejecutar el Proyecto SeveClieFrontend

Este documento proporciona los pasos para clonar y ejecutar el proyecto **SeveClieFrontend**, que utiliza Razor y jQuery para la gestión de clientes. **Antes de ejecutar el Frontend, es imprescindible que el Backend, el proyecto SeveClieBackend, esté en funcionamiento.**

---

## 1. Requisitos Previos

- **Git**: Asegúrate de tener Git instalado para clonar el repositorio.

Puedes verificar la instalación de Git ejecutando:

```bash
git --version
```

---

## 2. Ejecución del Backend (SeveClieBackend)

Clona y ejecuta el proyecto SeveClieBackend siguiendo sus propias instrucciones (consultar SeveClieBackend en [GitHub](https://github.com/AndrewBabativa/SeveClieBackend)).
---

## 3. Clonar el Proyecto SeveClieFrontend

Para clonar el repositorio del Frontend, sigue estos pasos:

1. Abre la terminal o línea de comandos.
2. Navega a la carpeta donde deseas clonar el proyecto.
3. Ejecuta el siguiente comando:

```bash
git clone https://github.com/AndrewBabativa/SeveClieFrontend.git
```

4. Una vez clonado el repositorio, navega al directorio del proyecto:

```bash
cd SeveClieFrontend
```

---

## 4. Ejecutar la Aplicación Frontend

El proyecto **SeveClieFrontend** utiliza Razor y jQuery. Para ejecutarlo:

1. Abre el proyecto en **Visual Studio**.
2. Compila y ejecuta la solución desde Visual Studio.
3. La aplicación se iniciará y podrás acceder a ella a través de tu navegador en la siguiente URL (o la configurada en el proyecto):

```
https://localhost:44371
```

---

## 5. Verificar la Ejecución del Backend

Es fundamental confirmar que el Backend se encuentra activo.  
Para ello:
- Abre tu navegador y accede a:
  
  ```
  https://localhost:44384/swagger/index.html
  ```

- Verifica que la documentación de la API se muestre correctamente, lo que indica que el **SeveClieBackend** está funcionando.
![image](https://github.com/user-attachments/assets/a92becf0-8fae-4a4d-95ec-1ef836cd585e)

---

## 2. Capturar la Pantalla de Inicio del Frontend

- Accede a la URL del Frontend (por ejemplo, `https://localhost:44371`).

![image](https://github.com/user-attachments/assets/bd121c06-50b7-4a00-8961-9e0df43028a9)

---

## 3. Proceso de Login

- En la página de inicio, ingresa las credenciales:  
  **Usuario:** `test`  
  **Contraseña:** `password`
- Haz clic en el botón **Login**.
- Una vez autenticado, se mostrará el módulo de gestión de clientes.
![image](https://github.com/user-attachments/assets/813d11a0-52bf-458e-8294-1aa29f96693c)

![image](https://github.com/user-attachments/assets/3706ff07-e9ae-4c29-9e39-05cf3e6856a3)

- Verificación de generación de token de autenticación :

![image](https://github.com/user-attachments/assets/3dee0f45-046e-462b-b083-886116ebefbd)




---

## 4. Módulo de Creación de Cliente

- Con el usuario autenticado, se mostrará el módulo de gestión de clientes.
- Llena el formulario de creación de cliente con datos de ejemplo (por ejemplo, Cédula, Nombre, Género, Fecha de Nacimiento y Estado Civil).
![image](https://github.com/user-attachments/assets/c9e9b51f-8ad3-445e-834c-ab70bb9c9838)

- Al dar clic en Crear y si los datos estan correctos se creara el regitro en BD:
![image](https://github.com/user-attachments/assets/7b84c62d-fd54-41e5-97b6-1d201ac13c67)


Y se mostrará el nuevo registro en la grilla de clientes :
![image](https://github.com/user-attachments/assets/7f3a8da2-bb10-444d-b840-717fd317a9b0)

---

## 5. Capturar el Módulo de Consulta de Clientes

- Haz clic en el botón para cargar la lista de clientes.
![image](https://github.com/user-attachments/assets/20a8f256-7b3b-4581-853f-4f21565b1614)

---

## 6. Capturar el Proceso de Edición de Cliente

- Selecciona un cliente de la lista y haz clic en el botón **Editar**.
- Se abrirá un modal con los datos precargados del cliente.
![image](https://github.com/user-attachments/assets/fe281129-3d1c-4050-8504-423768b77d6e)

- Opcionalmente, realiza cambios y guarda, luego captura nuevamente la pantalla de la tabla para mostrar la actualización.
![image](https://github.com/user-attachments/assets/cdee9676-870a-4fd6-be5f-5ce3772d3cbb)

![image](https://github.com/user-attachments/assets/2bcc860a-bde1-4696-a902-63bfbe82b05f)

Se confirma que en BD se actualizo el registro:

![image](https://github.com/user-attachments/assets/03ac0615-0543-45a2-81ce-bd5876d1eaf2)



---

## 7. Capturar el Proceso de Eliminación de Cliente

- En la lista de clientes, haz clic en el botón **Eliminar** de un cliente.
![image](https://github.com/user-attachments/assets/a49096b0-95b3-49ac-b6d1-d9e9da1b3e8a)

![image](https://github.com/user-attachments/assets/85eb81c5-5e4e-4efa-b1d8-8378f82bd423)

Se verifica en BD;

![image](https://github.com/user-attachments/assets/358ce6ee-92ba-4e44-8d05-ea5550080485)


---

## 8. Capturar el Uso del Filtro en la Tabla de Clientes

- Utiliza el campo de filtro para buscar clientes por nombre, cédula u otros atributos.
En este ejemplo se evidencian dos registros, en el texbox del filtro se puede ingresar cualquier atributo del cliente y este lo filtrará de manera inmediata

![image](https://github.com/user-attachments/assets/dda9dc3b-1159-496b-8f24-e2a258313483)

Ejemplo , por estado civil "solt"

![image](https://github.com/user-attachments/assets/952e4fc5-b5a5-4fbe-9f48-6ba93ea1a64d)

Ejemplo , por estado civil "menez"

![image](https://github.com/user-attachments/assets/bd99b10c-cfa7-4a88-84bf-68d7684d652a)

---
## Tecnologías Utilizadas

- **ASP.NET Core Razor Pages**:  
  Se utiliza para construir el frontend. Las vistas se generan en el servidor y se integran con lógica en C# para presentar contenido dinámico.

- **jQuery y AJAX**:  
  Se emplean para realizar solicitudes HTTP de forma asíncrona al backend, permitiendo la interacción sin necesidad de recargar la página. Esto facilita la realización de operaciones CRUD (crear, consultar, actualizar y eliminar) de forma dinámica.

- **Bootstrap**:  
  Utilizado para el diseño y la maquetación, ofreciendo una interfaz de usuario responsiva y moderna.
