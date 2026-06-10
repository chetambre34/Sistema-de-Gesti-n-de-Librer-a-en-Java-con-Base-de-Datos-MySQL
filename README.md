Fuentes del proyecto

| Tipo                |            Descripción                                                                                  |
|---------------------|---------------------------------------------------------------------------------------------------------|
| Institución         | Tecnología de Desarrollos de Sistemas Informáticos 2 - Semestre 2026                                    |
| Profesor            | Mag. Carlos Adolfo Beltrán Castro                                                                       |
| Estudiantes         | - Jhoan Sebastian Rodriguez Tamayo (C.C. 1005541707)<br>- Adrian Alejandro Lopez Niño (C.C. 1013592431) |
| Lenguaje            | Java                                                                                                    |
| IDE                 | NetBeans                                                                                                |
| Base de datos       | MySQL                                                                                                   |
| Conectividad        | JDBC                                                                                                    |
| Paradigma           | Programación Orientada a Objetos (POO)                                                                  |

---

  Características Generales del Proyecto

Nombre del proyecto
Sistema de Gestión de Librería en Java con Base de Datos MySQL

Objetivo
Desarrollar una aplicación de escritorio en Java que permita la gestión de una librería mediante operaciones CRUD (Crear, Leer, Actualizar, Eliminar), conectada a una base de datos MySQL.

 Estructura y navegación
El sistema cuenta con un menú principal que permite acceder a:
-  Usuarios (módulo base)
-  Libros (CRUD principal)
- Autores
- Editoriales
- Salir (con confirmación)

Cada opción abre un `JFrame` independiente para realizar operaciones específicas.

Funcionalidades principales
- CRUD de libros: Insertar, listar y eliminar libros.
- Conexión a base de datos: Mediante JDBC con validación de conexión.
- Menú de navegación: Acceso a formularios y cierre controlado.

Tecnologías utilizadas
- Java (NetBeans)
- MySQL
- JDBC
- JTable para visualización de datos
- JFrame para interfaces gráficas

 Pruebas realizadas
- Inserción de autores y editoriales
- Registro de libros
- Visualización en JTable
- Eliminación de registros
- Validación de conexión a MySQL

Instalación y ejecución
1. Instalar NetBeans, Java JDK y MySQL.
2. Crear la base de datos ejecutando el script proporcionado.
3. Configurar la conexión JDBC (usuario, contraseña, puerto).
4. Ejecutar el proyecto desde NetBeans.

Conclusión
Se logró desarrollar un sistema funcional aplicando conceptos de POO, bases de datos relacionales y operaciones CRUD.

---
 Base de Datos

Nombre de la base de datos: `librería`

 Tablas y estructuras

 Tabla `editorial`
| Campo        | Tipo | Descripción                         |
|--------------|------|-------------------------------------|
| id_editorial | PK   | Identificador único de la editorial |
| nombre       | -    | Nombre de la editorial              |

 Tabla `autor`
| Campo    | Tipo | Descripción                   |
|----------|------|-------------------------------|
| id_autor | PK   | Identificador único del autor |
| nombre   |  -   | Nombre del autor              |

 Tabla `libro`
| Campo             | Tipo | Descripción                       |
|-------------------|------|-----------------------------------|
| id_libro          | PK   | Identificador único del libro     |
| título            |   -  | Título del libro                  |
| fecha_publicacion |   -  | Fecha de publicación              |
| id_autor          | FK   | Relación con la tabla `autor`     |
| id_editorial      | FK   | Relación con la tabla `editorial` |

 Relaciones entre tablas
- Un autor puede tener varios libros → Relación 1 a N
- Una editorial puede publicar varios libros → Relación 1 a N
- Un libro pertenece a un autor y a una editorial → Relación N a 1

Diagrama relacional simplificado

```
autor (1) ──────< (N) libro (N) >────── (1) editorial
