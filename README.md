. Preparar el Backend
Abrir terminal en la carpeta backend

Navegar a: Entry-Level-Fullstack-Test/backend

Instalar dependencias (si no están instaladas)

npm install

Copy
Ejecutar migraciones de base de datos

npx sequelize-cli db:migrate

Copy
Esto crea la base de datos SQLite con todas las tablas necesarias

Iniciar el servidor backend

npm start

Copy
El servidor correrá en http://localhost:3001

Verás mensajes de conexión exitosa a la base de datos

2. Preparar el Frontend
Abrir NUEVA terminal en la carpeta frontend

Navegar a: Entry-Level-Fullstack-Test/frontend

Instalar dependencias (si no están instaladas)

npm install

Copy
Iniciar la aplicación React

npm start

Copy
La aplicación se abrirá automáticamente en http://localhost:3000

🧪 Cómo probar todas las funcionalidades
Funcionalidad 1: Registro de Usuario
Ve a http://localhost:3000

Haz clic en "Regístrate"

Llena el formulario con:

Nombre: Tu nombre

Apellidos: Tus apellidos

Email: cualquier email válido

Contraseña: mínimo 6 caracteres

Haz clic en "Registrarse"

Deberías ver mensaje de éxito y redirección al login

Funcionalidad 2: Inicio de Sesión
En la página principal (/)

Usa las credenciales que acabas de registrar

Haz clic en "Iniciar sesión"

Deberías ser redirigido al perfil

Funcionalidad 3: Vista de Perfil
Una vez logueado, verás:

Saludo con tu nombre

Tu email

Información del perfil (inicialmente vacía)

Haz clic en "Actualizar perfil"

Funcionalidad 4: Actualizar Información Personal
En modo edición, llena los campos:

Fecha de nacimiento

Tipo de documento (CC, TI, CE, PP)

Número de documento

Dirección

Teléfono

Nueva contraseña (opcional)

Contraseña actual (OBLIGATORIO)

Haz clic en "Guardar cambios"

Verás mensaje de confirmación

Funcionalidad 5: Cerrar Sesión
Haz clic en "Cerrar sesión"

Serás redirigido al login

El token se elimina automáticamente

Funcionalidad 6: Protección de Rutas
Prueba 1: Intenta acceder a /profile sin estar logueado → te redirige a /

Prueba 2: Estando logueado, intenta ir a / o /register → te redirige a /profile

✅ Requerimientos Funcionales Completados
✅ 1. Página de inicio con login
Formulario de login funcional

Validación de credenciales en base de datos

Manejo de errores

✅ 2. Enlace de registro
Texto "¿No tienes cuenta? Regístrate" presente

Enlace funcional a /register

✅ 3. Página de registro
Formulario completo con validaciones

Campos: Nombre, Apellidos, Email único, Contraseña segura

Mensaje de confirmación y redirección

✅ 4. Vista de perfil completa
Saludo personalizado con nombre y email

Formulario de actualización con todos los campos requeridos

Validación de contraseña actual obligatoria

Mensaje de confirmación al guardar

✅ 5. Protección de rutas
Redirección automática según estado de autenticación

Persistencia de sesión con localStorage

Verificación de token válido

🌟 Requerimientos Opcionales Implementados
✅ Registro de actividad del usuario
Se guarda IP y User Agent en cada login

Campos lastLoginIp y lastLoginUserAgent en base de datos

✅ Validación de datos
Frontend: React Hook Form con validaciones

Backend: Validaciones de email único, contraseñas, etc.

Mensajes de error descriptivos

✅ Diseño responsive
Material-UI garantiza responsividad

Funciona en móviles y desktop

🚀 Para la presentación
Puntos clave a mencionar:
Arquitectura completa:

Backend: Node.js + Express + Sequelize

Frontend: React + Material-UI + React Hook Form

Base de datos: SQLite (fácil de configurar)

Seguridad implementada:

Contraseñas hasheadas con bcrypt

JWT para autenticación

Validación de tokens

Protección de rutas

Experiencia de usuario:

Formularios con validación en tiempo real

Mensajes de error y éxito claros

Navegación intuitiva

Diseño responsive

Funcionalidades extra:

Registro de IP y User Agent

Persistencia de sesión

Validaciones robustas

🔧 Si algo no funciona
Problema: Error de base de datos
Solución: Ejecutar npx sequelize-cli db:migrate en la carpeta backend

Problema: Error de CORS
Solución: Asegurarse que el backend esté corriendo en puerto 3001

Problema: Página en blanco
Solución: Verificar que ambos servidores estén corriendo (3000 y 3001)

Problema: Token inválido
Solución: Hacer logout y login nuevamente

