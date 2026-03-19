### **Verbos HTTP y Acciones de la API (`product.routes.js` y `category.routes.js`)**

Para interactuar con nuestros recursos (productos y categorías), utilizamos los **Verbos HTTP**, que actúan como "órdenes" o "acciones" que el cliente le envía al servidor.

---

### **Rutas para Productos (`product.routes.js`)**

* **GET (Obtener):**
    * **Ruta `/` (`getAllProducts`):** Retorna la lista completa de productos.
    * **Ruta `/:id` (`getProductById`):** Retorna un producto específico según su ID.

* **POST (Crear):**
    * **Ruta `/` (`createProduct`):** Permite registrar un nuevo producto enviando datos como `name`, `price` y `category_id`.

* **PUT (Actualizar):**
    * **Ruta `/:id` (`updateProduct`):** Permite modificar un producto existente mediante su ID.

* **DELETE (Eliminar):**
    * **Ruta `/:id` (`deleteProduct`):** Elimina un producto del sistema según su ID.

---

### **Rutas para Categorías (`category.routes.js`)**

Este archivo define las rutas encargadas de gestionar las categorías del sistema.

* **GET (Obtener):**
    * **Ruta `/` (`getAllCategories`):** Retorna la lista completa de categorías.
    * **Ruta `/:id` (`getCategoryById`):** Retorna una categoría específica según su ID.

* **POST (Crear):**
    * **Ruta `/` (`createCategory`):** Permite registrar una nueva categoría enviando su nombre.

* **PUT (Actualizar):**
    * **Ruta `/:id` (`updateCategory`):** Permite modificar una categoría existente.

* **DELETE (Eliminar):**
    * **Ruta `/:id` (`deleteCategory`):** Elimina una categoría del sistema.

---

### **Resumen de Rutas (Endpoints)**

#### **Productos**

| Verbo | Ruta (URL) | Acción en el Controlador | Propósito |
| :--- | :--- | :--- | :--- |
| **GET** | `/` | `getAllProducts` | Listar todo el inventario. |
| **GET** | `/:id` | `getProductById` | Ver detalle de un producto. |
| **POST** | `/` | `createProduct` | Agregar un producto nuevo. |
| **PUT** | `/:id` | `updateProduct` | Editar un producto existente. |
| **DELETE** | `/:id` | `deleteProduct` | Eliminar un producto. |

---

#### **Categorías**

| Verbo | Ruta (URL) | Acción en el Controlador | Propósito |
| :--- | :--- | :--- | :--- |
| **GET** | `/` | `getAllCategories` | Listar todas las categorías. |
| **GET** | `/:id` | `getCategoryById` | Ver detalle de una categoría. |
| **POST** | `/` | `createCategory` | Crear una nueva categoría. |
| **PUT** | `/:id` | `updateCategory` | Actualizar una categoría. |
| **DELETE** | `/:id` | `deleteCategory` | Eliminar una categoría. |