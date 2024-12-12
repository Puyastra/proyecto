# Plataforma de Alquiler de Coches
Aplicación web para alquilar coches permitiendo a los usuarios encontrar, reservar alquileres de coches de manera rápida y segura.

## Características principales

- Búsqueda de vehículos por ubicación y fecha
- Filtrado avanzado por tipo de vehículo, precio y características
- Reservas instantáneas con confirmación inmediata

### Tecnologías utilizadas

| Componente | Tecnología |
|------------|------------|
| Frontend   | html/css |
| Backend    | PHP |
| Base de datos | MySQL |
| Autenticación | PHP Sessions |

link pagina web: [Automotive Rental Trends](https://www.alquilerdecoches.com/)

![RoadRover Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/Database-mysql.svg/724px-Database-mysql.svg.png)

## Ejemplo de código: Función para iniciar sesión en la página
```php
<?php
require_once "usuarioService.php";
session_start();
if ($_SERVER['REQUEST_METHOD'] == "POST") {
    $usuario = $_POST['usuario'];
    $password = $_POST['password'];
    if (login($usuario, $password)) {
        echo '<p><a href="/coches/index.php">Volver</a></p>';
    } else {
        echo '<p>Error al introducir el usuario</p>';
    }
}
?>
