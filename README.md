# Task Manager API

API RESTful para la gestión de tareas personales con autenticación JWT, verificación de correo electrónico y operaciones CRUD completas.

## 📋 Descripción

Proyecto personal desarrollado para la materia de Bases de Datos. Sistema de gestión de tareas que permite a los usuarios registrarse, verificar su correo electrónico, autenticarse mediante JWT y administrar sus tareas de forma segura.

## 🛠️ Stack Tecnológico

- **Java 17+**
- **Spring Boot 3**
  - Spring Web
  - Spring Data JPA
  - Spring Security
- **MySQL** - Base de datos relacional
- **JWT** - Autenticación stateless
- **Maven** - Gestión de dependencias y build

## ⚙️ Configuración

### Prerrequisitos
- Java 17 o superior
- Maven 3.6+
- MySQL 8.0+

### Variables de entorno

Configura tu `application.properties`:

```properties
# Base de datos
spring.datasource.url=jdbc:mysql://localhost:3306/taskmanager
spring.datasource.username=tu_usuario
spring.datasource.password=tu_password
spring.jpa.hibernate.ddl-auto=update

# JWT
jwt.secret=tu_clave_secreta_jwt
jwt.expiration=86400000

# Email (para verificación de registro)
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=tu_email@gmail.com
spring.mail.password=tu_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
```

🚀 Ejecución
bash
Copy
# Clonar el repositorio
git clone <url-del-repo>

# Navegar al directorio
cd Task-Manager-API

# Compilar y ejecutar
./mvnw spring-boot:run


🏗️ Arquitectura
```bash
src/main/java/university/jala/databaseApp/
├── components/         # Utilidades (JWT)
├── controllers/        # Capa de presentación (REST endpoints)
├── Dto/               # Objetos de transferencia de datos
├── entities/          # Modelos de dominio/JPA
├── repositories/      # Acceso a datos (Spring Data JPA)
├── security/          # Configuración de seguridad
├── services/          # Lógica de negocio
└── utils/             # Filtros y utilidades de seguridad
```
