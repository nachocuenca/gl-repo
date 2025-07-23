# Configuración de la zona privada

Este proyecto incluye una aplicación Laravel dentro de `private-zone` que utiliza [Filament](https://filamentphp.com/) para proporcionar un panel de administración.

## Requisitos
- PHP 8.2 o superior
- Composer

## Instalación
1. Desde la raíz del repositorio ejecuta:
   ```bash
   cd private-zone
   composer install
   cp .env.example .env
   php artisan key:generate
   php artisan migrate
   ```
2. Instala los assets y paneles de Filament:
   ```bash
   php artisan filament:install --panels --no-interaction
   ```
3. Crea un usuario administrador:
   ```bash
   php artisan make:filament-user --name="Admin" --email=admin@example.com --password=password
   ```

## Uso
Inicia el servidor de desarrollo:
```bash
php artisan serve
```
Luego accede a `http://localhost/admin` e inicia sesión con las credenciales creadas en el paso anterior.
