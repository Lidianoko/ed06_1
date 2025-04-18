# TaskMaster - Aplicación de Gestión de Tareas

## Descripción
TaskMaster es una aplicación diseñada para mejorar la productividad, permitiendo gestionar tareas demanera eficiente. Con esta herramienta, los usuarios pueden organizar sus actividades diarias demanera sencilla y eficaz.
## Características
* :heavy_check_mark: Creación y edición de tareas.
* Asignación de fechas límite y prioridades.
  * Prioridad baja, media y alta.
  * Fechas límite personalizadas con control de calendario.
* :open_file_folder: Organización en categorías y etiquetas.
* :white_check_mark: Marcar tareas como completadas.
* :bell: Notificaciones y recordatorios automáticos.
* :bar_chart: Visualización en lista y tablero Kanban.
## Instalación
Para instalar y ejecutar la aplicación, sigue los siguientes pasos:
```
# Clonar el repositorio
git clone https://github.com/usuario/taskmaster.git
cd taskmaster

# Instalar dependencias
npm install

# Ejecutar la aplicación
npm start
```
## Uso de la API
TaskMaster proporciona una API REST para gestionar tareas. A continuación, un ejemplo de cómocrear una tarea usando **JavaScript**:
```
fetch("https://api.taskmaster.com/tareas",{
  method:"POST",
  headers:{"Content-Type": "application/json" },
  body: JSON.stringify({titulo:"Nueva tarea", prioridad: "Alta"})
})
.then(response=>response.json())
.then(data=>console.log("Tarea creada:", data));
```
## Fórmula de Productividad
La eficiencia del usuario se calcula con la siguiente fórmula:

$$E = \frac{Tareas Completadas}{Tareas Totales}x100$$

Donde:
* $E$ es la eficiencia en porcentaje.
* $Tareas Completadas$ es el número de tareas finalizadas por el usuario.
* $Tareas Totales$ es el número total de tareas asignadas.
## Diagramas de Clases
La siguiente representación en UML muestra la estructura del sistema:

```mermaid
classDiagram
    class Usuario {
        - nombre: String
        - email: String
        + agregarTarea(tarea: Tarea): void
        + eliminarTarea(tarea: Tarea): void
    }

class Tarea {
        - titulo: String
        - prioridad: String
        - completada: Boolean
        + marcarComoCompletada(): void
    }

    Usuario "1" --> "*" Tarea: asigna
```
## Capturas de Pantalla
A continuación, una vista previa de la interfaz de usuario:

![image](https://github.com/user-attachments/assets/1e1a8c5b-9650-49c8-963e-955bc7e80dc5)

Para registrar una nueva tarea, sigue estos pasos:
1. Haz clic en el botón **Nueva Tarea**.
2. Completa el formulario con los datos de la tarea.
   1. **Título**: Nombre de la tarea.
   2. **Prioridad**: Nivel de importancia (baja, media, alta).
   3. **Fecha Límite**: Día y hora de vencimiento.
4. Haz clic en **Guardar** para crear la tarea.
5. ¡Listo! La tarea se ha registrado correctamente.

Si deseas que el título de la tarea sea visible en negrita, escríbelo entre dobles asteriscos: \*\*Título de la Tarea\*\*.
## Histoial de versiones
En la siguiente tabla se muestran las versiones publicadas de la aplicación:
| Versión| Fecha       | Descripción            |
| -----: | :-----:     | :--------------------- |
| 1.0.0  | 01/01/2024  | Lanzamiento inicial    |
| 1.1.0  | 15/01/2024  | Nuevas funcionalidades | 
| 1.1.1  | 30/01/2024  | Corrección de errores  | 
| 1.2.0  | 15/02/2024  | Mejoras de rendimiento | 
| 2.0.0  | 15/03/2024  | Versión estable        | 
| 2.1.0  | 30/03/2024  | Corrección de errores  | 
| 2.2.0  | 15/04/2024  | Mejoras de usabilidad  | 
| 2.3.0  | 30/04/2024  | Nuevas funcionalidades | 
## Créditos
Desarrollado por [Lidia Nokonoko](https://github.com/Lidianoko)
## Licencia
Este proyecto está bajo la Licencia MIT.
