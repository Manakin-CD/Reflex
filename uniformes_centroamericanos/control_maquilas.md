# Documentación de la Aplicación de Gestión de Maquilas

## 1. Funcionalidades Principales

### a) Panel de Administración

#### Ingresar Datos:
- Nombre de la maquila.
- Capacidad máxima de piezas.
- Fecha de entrega.
- Fecha de culminación.
- Estado (escogido por colores).

#### Modificar Datos:
- Actualización de las piezas asignadas a la maquila.
- Cambiar el estado manualmente según el progreso.

### b) Pantalla Principal
- Visualizar las maquilas en cuadros, con:
  - **Nombre**.
  - **Capacidad total**.
  - **Cantidad de piezas procesadas/restantes**.
  - **Color según el estado**.

#### Cambios Automáticos de Colores Según Fechas Configuradas:
- **Verde**: Capacidad total disponible.
- **Amarillo**: Trabajo asignado (en producción).
- **Naranja**: Días antes de la fecha de culminación.
- **Azul**: Trabajo listo para recoger.
- **Rojo**: Fecha de culminación sobrepasada.

---

## 2. Stack y Arquitectura

- **Frontend**: Reflex (para diseño responsivo e interactivo).
- **Backend**: FastAPI (para APIs rápidas y ligeras).
- **Base de datos**: PostgreSQL (para almacenar información de las maquilas y pedidos).
- **Deploy**: Utilizar servicios como Vercel o AWS.

---

## 3. Componentes de la Aplicación

### a) Página Principal
- Lista de maquilas renderizada dinámicamente:
  - Cada cuadro muestra:
    - **Nombre de la maquila**.
    - **Capacidad actual**.
    - **Estado con su color asociado**.
  - **Cálculo dinámico del estado** según las fechas configuradas.

### b) Panel de Administración
- Formulario para:
  - Añadir nuevas maquilas.
  - Actualizar detalles de una maquila existente.
  - Cambiar el estado de forma manual.
