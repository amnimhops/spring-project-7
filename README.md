# spring-class-project-7

#### Descripción del Proyecto
El objetivo de este proyecto es desarrollar una API REST para la gestión de una filmoteca online. La API permitirá a los usuarios no identificados realizar consultas sobre las películas disponibles (operaciones GET), mientras que las acciones de agregar, actualizar y eliminar películas (operaciones POST, PUT y DELETE) requerirán que el usuario esté autenticado y tenga el rol de administrador. 

#### Objetivos
1. Desarrollar una API REST utilizando Java y Spring Boot para gestionar una filmoteca.
2. Implementar autenticación y autorización con Spring Security, utilizando un rol fijo de administrador.
3. Crear vistas dinámicas y plantillas con Thymeleaf para la interacción del usuario.
4. Proteger las rutas y acciones de la API con los roles especificados.
5. Proporcionar una interfaz de usuario amigable para la gestión de películas.

#### Artefactos a Diseñar

1. **Entidades**:
   - Film

2. **Controladores**:
   - FilmController

3. **Servicios**:
   - FilmService

4. **Repositorios**:
   - FilmRepository

5. **Configuración de Seguridad**:
   - Configuración de Spring Security

6. **Vistas Thymeleaf**:
   - Listado de películas
   - Formulario para agregar/editar películas
   - Página de inicio de sesión

>Nota: Los nombres de los artefactos son orientativos

#### Pasos en Orden a Seguir

1. **Configuración del Proyecto**:
   - Crear una nueva aplicación Spring Boot.
   - Configurar las dependencias necesarias para Spring Boot, Spring Security y Thymeleaf.

2. **Modelado de Entidades**:
   - Crear la entidad `Film` con atributos como id, título, director, año, género, y sinopsis.

3. **Creación de Repositorios**:
   - Crear el repositorio `FilmRepository` para las operaciones CRUD de películas.

4. **Desarrollo de Servicios**:
   - Implementar `FilmService` para la lógica de negocio relacionada con películas.

5. **Implementación de Controladores**:
   - Crear `FilmController` con endpoints para las operaciones CRUD:
     - GET /films
     - GET /films/{id}
     - POST /films (solo para administradores)
     - PUT /films/{id} (solo para administradores)
     - DELETE /Films/{id} (solo para administradores)

6. **Configuración de Seguridad**:
   - Configurar Spring Security para la autenticación de usuarios predefinidos.
   - Definir un administrador con rol `ADMIN`.
   - Configurar las rutas para permitir solo a los administradores realizar operaciones POST, PUT y DELETE.

7. **Desarrollo de Vistas con Thymeleaf**:
   - Crear plantillas Thymeleaf para:
     - Listado de películas (público)
     - Formulario de agregar/editar películas (administrador)
     - Página de inicio de sesión

8. **Consideraciones adicionales**:
   - Este proyecto es para explorar los mecanismos de autenticación básica de Spring Security. En caso de duda, optar por la solución más sencilla.
   - La gestión de permisos y roles se puede hacer directamente en el código, no es necesario crear tablas de usuarios ni roles ya que solo existe un rol especial, el administrador.
   - En caso de invocar un endpoint sin los privilegios adecuados, la aplicación arrojará un error 403
  


#### Bibliografía Básica
1. **Documentación de Spring Boot**: [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)
2. **Documentación de Spring Security**: [https://spring.io/projects/spring-security](https://spring.io/projects/spring-security)
3. **Guía de Thymeleaf**: [https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html](https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html)
4. **API REST en Spring Boot**: [https://spring.io/guides/tutorials/rest/](https://spring.io/guides/tutorials/rest/)
5. **Spring Security y Roles**: [https://www.baeldung.com/role-and-privilege-for-spring-security-registration](https://www.baeldung.com/role-and-privilege-for-spring-security-registration)
