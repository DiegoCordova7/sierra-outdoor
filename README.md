# Sierra Outdoor

Tienda virtual desarrollada con **OpenCart** para el proyecto académico de la materia **Sistemas de Comercio Electrónico**.

Sierra Outdoor está enfocada en la venta de productos y accesorios para **camping, senderismo y actividades al aire libre**.

---

## Equipo

| Integrante                          | Responsabilidad                                           |
| ----------------------------------- | --------------------------------------------------------- |
| **Diego Emilio Córdova**            | Coordinación técnica, instalación y configuración general |
| **Arturo de Jesús Galván**          | Catálogo, categorías y productos                          |
| **Cristal Alejandra Arvayo**        | Diseño visual, imágenes y contenido                       |
| **Álvaro Alejandro Arriaga Ortega** | Carrito, usuarios, checkout y pruebas                     |

---

## Tecnologías

- **OpenCart 3.0.4.1**
- **PHP**
- **MariaDB**
- **Apache**
- **XAMPP**
- **HTML / CSS / JavaScript**
- **Git / GitHub**

---

## Requisitos

Para ejecutar el proyecto localmente se necesita:

- XAMPP
- Apache
- MariaDB / MySQL
- PHP compatible con OpenCart 3.0.4.1
- Git

---

## Instalación local

### 1. Clonar el repositorio

Desde la carpeta `htdocs` de XAMPP:

```bash
git clone <URL_DEL_REPOSITORIO> sierra-outdoor
```

La estructura deberá quedar:

```text
xampp/
└── htdocs/
    └── sierra-outdoor/
```

### 2. Configurar la base de datos

Crear una base de datos llamada:

```text
sierra_outdoor
```

Utilizar una codificación compatible con OpenCart, preferentemente:

```text
utf8mb4
```

Después importar el archivo SQL proporcionado con el proyecto:

```text
sierra_outdoor.sql
```

### 3. Configurar OpenCart

Crear los archivos de configuración a partir de sus archivos de distribución:

```text
config-dist.php → config.php
admin/config-dist.php → admin/config.php
```

Los archivos `config.php` y `admin/config.php` **no se almacenan en GitHub**, ya que contienen configuración específica de cada instalación.

Cada integrante debe configurar sus propios datos de conexión a MariaDB.

Ejemplo de configuración local:

```text
Database Driver: MySQLi
Database Host: 127.0.0.1
Database Port: 3308
Database User: root
Database Password: [local]
Database Name: sierra_outdoor
Database Prefix: oc_
```

> El puerto puede ser diferente dependiendo de la configuración de XAMPP de cada integrante.

### 4. Ejecutar la tienda

Con Apache y MariaDB activos, abrir:

```text
http://localhost/sierra-outdoor/
```

Para acceder al panel administrativo:

```text
http://localhost/sierra-outdoor/admin/
```

---

## Configuración actual

La instalación principal utiliza:

- **Moneda:** Mexican Peso (MXN)
- **País:** México
- **Región:** Sonora
- **Impuesto:** IVA 16%
- **Envío:** Tarifa fija de $99 MXN
- **Método de pago:** Cash On Delivery
- **SEO URLs:** Activadas

La configuración puede variar ligeramente en las instalaciones locales de cada integrante.

---

## Organización del proyecto

Las principales áreas de trabajo son:

### Catálogo

- Categorías
- Productos
- Precios
- Descripciones
- Inventario

Responsable: **Arturo**

### Diseño y contenido

- Logo
- Imágenes
- Contenido visual
- Apariencia general de la tienda

Responsable: **Cristal**

### Compra y pruebas

- Usuarios
- Carrito
- Checkout
- Métodos de pago
- Pruebas de compra

Responsable: **Álvaro**

### Configuración técnica

- Instalación
- Base de datos
- Configuración general
- Servidor
- Integración
- Control de versiones

Responsable: **Diego**

---

## Flujo de trabajo con Git

Antes de comenzar a trabajar:

```bash
git pull
```

Después de realizar cambios:

```bash
git status
git add .
git commit -m "Descripción del cambio"
git push
```

### Ejemplos de commits

```bash
git commit -m "Agrega productos de camping"
```

```bash
git commit -m "Actualiza imágenes del catálogo"
```

```bash
git commit -m "Configura checkout"
```

```bash
git commit -m "Actualiza diseño de la tienda"
```

### Importante

No subir:

- Contraseñas
- Credenciales de base de datos
- `config.php`
- `admin/config.php`
- Logs
- Cachés
- Archivos temporales
- Datos personales reales de clientes

El archivo `.gitignore` se encarga de excluir estos archivos cuando corresponde.

---

## Base de datos

La aplicación utiliza MariaDB/MySQL.

Nombre de la base de datos:

```text
sierra_outdoor
```

La base de datos **no se sincroniza mediante Git**.

Cuando sea necesario compartir cambios importantes de la base de datos, se debe generar un nuevo respaldo SQL y comunicar al equipo qué cambios contiene.

---

## Prueba de compra

Una vez configurado el catálogo, se debe comprobar el flujo completo:

```text
Inicio
  ↓
Categoría
  ↓
Producto
  ↓
Agregar al carrito
  ↓
Checkout
  ↓
Dirección
  ↓
Envío
  ↓
Método de pago
  ↓
Confirmar pedido
  ↓
Pedido generado
```

La prueba debe verificar que:

- El producto se agregue correctamente.
- El precio sea correcto.
- El IVA se calcule correctamente.
- El costo de envío aparezca.
- El método de pago esté disponible.
- El pedido se genere correctamente.

---

## Estructura principal

```text
sierra-outdoor/
├── admin/
├── catalog/
├── extension/
├── image/
├── install/
├── system/
├── .gitignore
├── .htaccess
├── index.php
└── README.md
```

---

## Proyecto académico

Proyecto desarrollado para la materia:

**Sistemas de Comercio Electrónico — 2026-2**

**Equipo 1 — Sierra Outdoor**

Tienda virtual orientada a productos para camping, senderismo y actividades al aire libre.
