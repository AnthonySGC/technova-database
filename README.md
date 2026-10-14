# TechNova - Control de Versiones de Bases de Datos

## Descripcion

Proyecto academico de la asignatura Administracion y Gestion
de Bases de Datos de la Universidad Americana (UAM).

Implementa el control de versiones de las bases de datos
TechNova_Central y TechNova_Bodega mediante scripts SQL,
utilizando Git y GitHub.

## Tecnologias utilizadas

- Microsoft SQL Server 2025
- SQL Server Management Studio (SSMS)
- Git
- GitHub
- Transact-SQL (T-SQL)

## Estructura del proyecto

TechNova-DB/
|-- database/
|   |-- baseline/
|   |   `-- V1.0__TechNova_inicial.sql
|   `-- migrations/
|       |-- V1.1__agregar_fecha_actualizacion_productos.sql
|       |-- V1.2__indice_productos_activos.sql
|       |-- V1.3__actualizar_catalogo_productos.sql
|       |-- V1.4__agregar_marca_productos.sql
|       `-- V1.4.1__actualizar_catalogo_con_marca.sql
|-- queries/
|-- documentation/
|-- .gitignore
|-- CHANGELOG.md
`-- README.md

## Historial de versiones

### v1.0 - Estructura inicial
Creacion de las bases de datos TechNova_Central y TechNova_Bodega.

### v1.1 - Fecha de actualizacion
Se agrega FechaUltimaActualizacion a inventario.Productos.

### v1.2 - Indice de productos
Se crea el indice IX_Productos_Activo.

### v1.3 - Actualizacion del catalogo
Se modifica inventario.vw_CatalogoProductos para incorporar
FechaUltimaActualizacion.

### v1.4 - Marca de productos
Se agrega Marca NVARCHAR(80) a inventario.Productos.

### v1.4.1 - Actualizacion complementaria
Se actualiza la vista del catalogo para mostrar Marca.

## Ejecucion

1. Abrir SQL Server Management Studio.
2. Conectarse a una instancia de SQL Server 2025.
3. En un entorno nuevo de pruebas, ejecutar el script baseline.
4. Ejecutar las migraciones SQL en orden de version.
5. Verificar los cambios mediante consultas SQL.

IMPORTANTE:
El script baseline elimina y vuelve a crear ambas bases
de datos. No debe ejecutarse sobre bases con informacion
que se necesite conservar.

Las migraciones ya aplicadas no deben ejecutarse nuevamente
sin comprobar previamente el estado de la base de datos.

## Control de versiones

Git permite registrar los cambios estructurales mediante
commits, ramas y etiquetas de version.

La rama main contiene la version integrada del proyecto.

La rama feature-productos se utilizo localmente para
desarrollar los cambios correspondientes a la version 1.4.

## Registro de cambios

Consultar CHANGELOG.md para conocer las modificaciones
realizadas en cada version.
