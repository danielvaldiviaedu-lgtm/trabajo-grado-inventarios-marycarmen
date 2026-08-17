# Arquitectura Modelo-Vista-Controlador (MVC)

El patrón de arquitectura **Modelo-Vista-Controlador (MVC)** es un patrón de diseño de software que separa los datos y la lógica de negocio de una aplicación de su representación visual y el módulo encargado de gestionar los eventos y las comunicaciones. Para ello, MVC propone la construcción de tres componentes distintos que son el modelo, la vista y el controlador.

## Componentes del MVC

### 1. Modelo (Model)
Es el componente responsable de gestionar los datos, la lógica y las reglas de negocio de la aplicación. 
* **Responsabilidades:** Acceso a bases de datos, actualización de estados, validaciones y lógica de la información.
* **Comunicación:** Notifica a la vista y al controlador sobre cambios en su estado. No sabe nada de la interfaz de usuario.

### 2. Vista (View)
Es la representación visual de los datos (la interfaz de usuario). 
* **Responsabilidades:** Mostrar la información al usuario de forma gráfica o textual. Recopila la interacción del usuario (clics, entradas de texto, etc.).
* **Comunicación:** Obtiene los datos del modelo para mostrarlos y envía las interacciones del usuario al controlador.

### 3. Controlador (Controller)
Actúa como intermediario entre el Modelo y la Vista.
* **Responsabilidades:** Gestiona las peticiones del usuario, procesa las entradas recibidas por la Vista, invoca al Modelo para realizar las acciones pertinentes, y finalmente selecciona la Vista adecuada para mostrar los resultados.
* **Comunicación:** Escucha los eventos de la vista (ej. botón presionado), actualiza el modelo según sea necesario y actualiza la vista con los nuevos datos.

## Flujo de Trabajo Típico
1. El usuario interactúa con la **Vista** (por ejemplo, hace clic en un botón).
2. El **Controlador** recibe la notificación de la acción desde la vista.
3. El **Controlador** accede al **Modelo**, actualizando sus datos u obteniendo nueva información según la acción del usuario.
4. El **Modelo** realiza la operación y puede notificar los cambios.
5. La **Vista** se actualiza (ya sea a través del controlador o consultando directamente el modelo modificado) mostrando la nueva información al usuario.

## Ventajas de usar MVC
- **Separación de responsabilidades:** Cada componente tiene una tarea específica, lo que facilita el mantenimiento, la lectura y la escalabilidad del sistema.
- **Reusabilidad de código:** Las vistas y los modelos pueden reutilizarse sin afectar a otros componentes.
- **Facilidad de pruebas (Testing):** Al estar separada la lógica de la interfaz, es mucho más sencillo realizar pruebas unitarias sobre el modelo y el controlador.
- **Trabajo en equipo simultáneo:** Permite que diferentes desarrolladores (ej. diseñadores Frontend y programadores Backend) trabajen al mismo tiempo en Vistas y Modelos sin interferir entre sí.
