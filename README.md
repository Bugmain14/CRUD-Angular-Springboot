# Gestión de Empleados - API REST

API REST para gestionar empleados (crear, listar, consultar, actualizar y eliminar), desarrollada con Spring Boot. El frontend en Angular está en [CRUD-Angular-Springboot-frontend](https://github.com/Bugmain14/CRUD-Angular-Springboot-frontend).

## Tecnologías

- Java 17 y Spring Boot 3.4
- Spring Data JPA y Bean Validation
- MySQL
- Lombok y Maven

## Arquitectura

```
empleados-backend/src/main/java/ac/empleados/
├── controller/   Endpoints REST
├── service/      Lógica de negocio
├── repository/   Acceso a datos con JPA
├── model/        Entidad Employee
├── dto/          Datos de entrada con validaciones
└── exception/    Manejo global de errores
```

## Endpoints

| Método | Ruta | Descripción |
|---|---|---|
| GET | `/employees` | Listar empleados |
| GET | `/employees/{id}` | Consultar un empleado |
| POST | `/employees` | Crear empleado |
| PUT | `/employees/{id}` | Actualizar empleado |
| DELETE | `/employees/{id}` | Eliminar empleado |

## Cómo ejecutarlo

1. Crea la base de datos `employeesystem` en MySQL.
2. Define las credenciales en las variables de entorno `DB_USERNAME` y `DB_PASSWORD`.
3. Ejecuta:

```bash
cd empleados-backend
./mvnw spring-boot:run
```

La API queda disponible en `http://localhost:8080`.
