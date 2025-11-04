# Proyecto StorageApp

## 1. Decisiones de Diseño

- Se utilizó Laravel como framework backend.
- Vanilla JavaScript para las interacciones del usuario sin recargar la página.
- Sistema de cuotas por usuario y por grupo.
- Validación de extensiones prohibidas, incluyendo inspección de archivos ZIP.
- Interfaz de administración para gestionar usuarios, grupos y extensiones.
- Sistema de autenticación y roles (Admin / User).

## 2. Instalación y Configuración

1. Clonar el repositorio:
```bash
git clone <https://github.com/Harvey-46904/almacenamientoseguro.git>
cd <almacenamientoseguro>
```

2. Instalar dependencias de PHP:
```bash
composer install
```

3. Copiar el archivo de entorno:
```bash
cp .env.example .env
```

4. Configurar `.env` con la información de tu base de datos y otras variables.

5. Generar la clave de la aplicación:
```bash
php artisan key:generate
```

6. Migrar la base de datos y ejecutar seeders:
```bash
php artisan migrate --seed
```

7. Configurar permisos de almacenamiento (si usas almacenamiento público):
```bash
php artisan storage:link
```

8. Ejecutar el servidor local:
```bash
php artisan serve
```

## 3. Credenciales de Ejemplo

| Nombre | Email | Rol | Contraseña |
|--------|-------|-----|------------|
| Hache | hache@secure.com | User | 123456789 |
| Administrador Principal | administracion@secure.com | Admin | 123456789 |

## 4. Notas Adicionales

- Las cuotas de usuario pueden ser personalizadas o heredadas del grupo.
- Los archivos subidos se almacenan en `storage/app/public/uploads/{user_id}`.
- Se debe tener cuidado con las extensiones prohibidas al subir archivos.

