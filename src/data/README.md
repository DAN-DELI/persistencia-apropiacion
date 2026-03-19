## **Capa de Datos**

Esta capa representa nuestra **Fuente de Datos**. En un desarrollo profesional, aquí es donde conectaríamos con una base de datos real (como MySQL o PostgreSQL). Para este ejercicio, utilizamos un **arreglo de objetos en memoria** que actúa como nuestro almacén temporal.

---

#### **Estructura del Objeto "Producto" (`products.data.js`)** 

Para que el sistema funcione correctamente, cada producto dentro del arreglo debe seguir la misma estructura (esquema). Esto permite que el Modelo y el Controlador puedan procesar la información sin errores:

* **`id` (Número):** Es el identificador único. Funciona como la "cédula" del producto; no puede haber dos iguales. Es fundamental para las operaciones de búsqueda y eliminación.
* **`name` (Texto):** El nombre descriptivo del artículo tecnológico.
* **`price` (Número):** El costo del producto. Se maneja como número para poder realizar operaciones matemáticas (como sumas de totales o filtros de precios).
* **`category_id` (Número):** Llave foranea la cual representa la categoria a la cual pertenece el producto.  


---

#### **Estructura del Objeto "Categoría" (`categories.data.js`)** 

Al igual que los productos, las categorías siguen una estructura definida. Estas permiten organizar los productos y establecer relaciones entre ellos:

* **`id` (Número):** Es el identificador único de la categoría. No puede repetirse y es utilizado como referencia en los productos mediante el `category_id`.
* **`name` (Texto):** Es el nombre de la categoría. Describe el tipo de productos que agrupa (por ejemplo: "Periféricos", "Audio", etc.).

---

#### **Relación entre Productos y Categorías**

El campo **`category_id`** dentro del objeto producto actúa como una **llave foránea**, lo que significa que:

* Cada producto está asociado a una categoría existente.
* El valor de `category_id` debe coincidir con el `id` de alguna categoría en `categories.data.js`.

Esto permite:

* Filtrar productos por categoría.
* Organizar mejor la información.
* Simular relaciones como en una base de datos real.

