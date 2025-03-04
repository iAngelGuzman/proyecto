# Creación de la base de datos

```
CREATE DATABASE plantsvszombies;
```

Seleccionar la base de datos para agregar mas datos.
```
USE plantsvszombies;
```

Crear tabla de usuarios.
```
CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario VARCHAR(50) UNIQUE NOT NULL,
    contrasena VARCHAR(255) NOT NULL,
    rol VARCHAR(25) NOT NULL
);
```

Crear tabla de almanaque.
```
CREATE TABLE almanaque (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100),
    descripcion TEXT,
    imagen VARCHAR(255)
);
```

Agregar usuarios con su respectivo rol.
```
INSERT INTO usuarios (usuario, contrasena, rol)
VALUES ('admin', 'root', 'admin');

INSERT INTO usuarios (usuario, contrasena, rol)
VALUES ('usuario', 'root', 'usuario');
```

Agregar plantas al almanaque.
```
INSERT INTO almanaque (nombre, descripcion, imagen)
VALUES ('Lanzaguisantes', 'planta', 'null');

INSERT INTO almanaque (nombre, descripcion, imagen)
VALUES ('Planta Carnivora', 'planta', 'null');

INSERT INTO almanaque (nombre, descripcion, imagen)
VALUES ('Online', 'online image', 'https://static.wikia.nocookie.net/plantsvszombies/images/2/25/HD_Repeater.png/revision/latest?cb=20221011165152');
```
