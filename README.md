# Welmo Backend  
Backend del sistema de mensajería multicanal y multiusuario Welmo.

Welmo es una plataforma diseñada para centralizar la comunicación con clientes a través de múltiples canales (WhatsApp, Webchat, Email, etc.) y permitir la operación multiusuario y multiempresa con atención en tiempo real.

Este repositorio contiene la API REST, servicios, WebSockets y la capa de negocio que soporta el panel administrativo de Welmo.

------------------------------------------------------------
Tecnologías principales
------------------------------------------------------------
- Node.js
- TypeScript
- Express.js
- Sequelize ORM
- MySQL
- Redis
- Socket.IO
- JWT Authentication

------------------------------------------------------------
Estructura principal del backend
------------------------------------------------------------
src/
 ├── app.ts               (Configuración principal de Express)
 ├── server.ts            (Inicialización del servidor)
 ├── config/              (Config de DB, Redis y variables)
 ├── controllers/         (Controladores de API)
 ├── database/
 │    ├── models/         (Modelos Sequelize)
 │    ├── migrations/     (Migraciones de base de datos)
 ├── services/            (Lógica de negocio)
 ├── jobs/                (Procesos en background)
 ├── utils/               (Helpers y funciones comunes)
 └── sockets/             (Socket.IO / WebSockets)

------------------------------------------------------------
Configuración del entorno
------------------------------------------------------------
Crea un archivo .env basado en .env.example con valores como:

DB_HOST=
DB_USER=
DB_PASS=
DB_NAME=
JWT_SECRET=
REDIS_HOST=
REDIS_PORT=

------------------------------------------------------------
Base de datos
------------------------------------------------------------
Ejecuta las migraciones:

npx sequelize db:migrate

------------------------------------------------------------
Ejecutar en desarrollo
------------------------------------------------------------
Instalar dependencias:

npm install

Iniciar servidor en modo desarrollo:

npm run dev

------------------------------------------------------------
Ejecutar en producción
------------------------------------------------------------
Compilar:

npm run build

Ejecutar:

npm start

------------------------------------------------------------
Socket.IO (tiempo real)
------------------------------------------------------------
El sistema usa WebSockets para:

- Actualización de tickets
- Recepción de mensajes entrantes
- Indicadores de “typing”
- Sincronización en tiempo real entre agentes

------------------------------------------------------------
Integraciones actuales
------------------------------------------------------------
- WhatsApp (sesiones QR, multi-instancia)
- Mensajería interna
- Multiempresa (tenants)
- Multiusuario (roles y permisos)
- Tickets y comunicación en tiempo real

------------------------------------------------------------
Seguridad
------------------------------------------------------------
- JWT para autenticación
- Control de roles (admin, user, support)
- Rate limiting opcional vía Redis
- Sanitización básica de inputs

------------------------------------------------------------
Endpoints (documentación)
------------------------------------------------------------
Documentación OpenAPI/Swagger en proceso de actualización.

------------------------------------------------------------
Licencia
------------------------------------------------------------
Este proyecto es parte de la plataforma Welmo desarrollada por Muto Estudio Digital.
No está autorizado su uso, distribución o comercialización sin aprobación previa.

------------------------------------------------------------
Contacto
------------------------------------------------------------
📧 contacto@mutoestudio.com
🌐 https://mutoestudio.com
