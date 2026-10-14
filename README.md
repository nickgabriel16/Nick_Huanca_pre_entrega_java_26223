Sistema de Gestión de Artículos

Aplicación de consola en Java desarrollada para la preentrega de Programación Orientada a Objetos (POO). El sistema permite administrar artículos comerciales (electrónicos y alimenticios) mediante una colección dinámica en memoria.



🎯 Objetivos y Conceptos Aplicados
Herencia (extends): Reutilización de atributos y métodos comunes a partir de la clase base Articulo.
Clases y Métodos Abstractos: Definición de Articulo como clase abstracta con los métodos getTipoArticulo() y getDetalleEspecifico().
Polimorfismo: Almacenamiento y manipulación homogénea de diferentes subtipos en un único ArrayList<Articulo>.
Sobrescritura de Métodos (@Override): Implementación especializada de toString() y de los métodos abstractos en cada subclase.
Uso de super y this: Delegación a constructores y métodos de la superclase.
Encapsulamiento: Atributos privados accesibles únicamente mediante getters y setters.
Identificación de Tipos (instanceof y casting): Modificación condicional de atributos propios de cada subtipo.
Validaciones y Control de Errores: Manejo de entradas numéricas y cadenas no vacías con Scanner y bloques try-catch.


📁 Estructura del Proyecto
text
herencia_polimorfismo_tostring/
├── src/
│   └── com/
│       └── techlab/
│           └── articulo/
│               ├── App.java
│               └── model/
│                   ├── Articulo.java
│                   ├── ArticuloElectronico.java
│                   ├── ArticuloAlimenticio.java
│                   └── Categoria.java
├── bin/                 # Archivos compilados (.class)
└── README.md

Descripción de Clases

Categoria: Representa la categoría del artículo (código, nombre, descripción).
Articulo (abstracta): Superclase con los datos comunes (código, nombre, precio, categoría).
ArticuloElectronico: Subclase con atributo propio garantiaMeses y método de soporte técnico.
ArticuloAlimenticio: Subclase con atributo propio diasParaVencimiento.
App: Clase principal que controla el flujo de consola, precarga de categorías, menú y métodos de lectura con validación.
📋 Funcionalidades del Menú
text
======================================================
SISTEMA DE ARTÍCULOS - CLASE 4 (HERENCIA Y TO_STRING)
======================================================
1 - Ingresar artículo
2 - Listar artículos
3 - Consultar un artículo
4 - Modificar un artículo
5 - Eliminar un artículo
6 - Listar categorías
0 - Salir
======================================================
Ingresar artículo: Permite elegir el subtipo (electrónico o alimenticio), valida que el código no esté duplicado, que el precio sea no negativo y que la categoría seleccionada exista.
Listar artículos: Recorre la lista invocando polimórficamente el método toString().
Consultar un artículo: Busca por código y muestra su detalle específico y mesa de ayuda (si aplica).
Modificar un artículo: Modifica nombre, precio, categoría y el atributo específico del subtipo mediante instanceof.
Eliminar un artículo: Remueve el artículo de la lista por código.
Listar categorías: Muestra las categorías precargadas en el sistema.
Salir: Finaliza la ejecución y cierra los recursos.
