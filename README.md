# ClinicaDent

Aplicación web para gestionar tratamientos y reservas de una clínica dental. El sistema permite consultar los servicios disponibles, solicitar una cita según los horarios libres y revisar la agenda desde un calendario administrativo.

## Funcionalidades principales

### Para pacientes

- Consulta del catálogo de tratamientos con imagen y descripción.
- Reserva de citas mediante un formulario con datos de contacto.
- Selección del tratamiento, la fecha y la hora de atención.
- Cálculo dinámico de horarios disponibles según la duración del tratamiento y las citas registradas.
- Validación de los datos ingresados y confirmación del resultado de la reserva.

### Para administración

- Registro de tratamientos con título, descripción, duración e imagen.
- Carga de imágenes para el catálogo.
- Visualización mensual de las citas en un calendario.
- Conteo de citas por día.
- Consulta de la hora, el tratamiento y los datos de contacto asociados a cada reserva.

## Flujo del sistema

1. Los tratamientos registrados se muestran en el catálogo y en el formulario de reserva.
2. El paciente selecciona un tratamiento y una fecha laborable disponible.
3. El sistema consulta las citas existentes y calcula los horarios compatibles con la duración elegida.
4. La reserva se almacena en la base de datos.
5. El personal de la clínica puede consultar la agenda y el detalle de las citas desde el calendario administrativo.

## Tecnologías

| Área | Tecnologías |
| --- | --- |
| Backend | PHP |
| Frontend | HTML5, CSS3 y JavaScript |
| Interactividad | jQuery y AJAX |
| Interfaz | Bootstrap y Semantic UI |
| Base de datos | PostgreSQL |

## Características técnicas

- Aplicación web cliente-servidor desarrollada con PHP procedural.
- Persistencia de tratamientos y citas en PostgreSQL.
- Endpoints PHP para consultar citas, detalles y disponibilidad de horarios mediante AJAX.
- Actualización dinámica del calendario y de los selectores de fecha y hora.
- Cálculo de disponibilidad en intervalos de 15 minutos, considerando la duración de cada tratamiento y las reservas existentes.
- Generación de fechas de atención en días laborables.
- Almacenamiento de imágenes en el sistema de archivos y referencia desde la base de datos.
- Interfaces diferenciadas para la consulta pública y la gestión administrativa.

## Módulos principales

- **Inicio:** acceso a la reserva de citas, el catálogo y el área administrativa.
- **Tratamientos:** publicación y consulta de los servicios ofrecidos.
- **Reservas:** registro de pacientes y asignación de horarios disponibles.
- **Agenda:** calendario mensual con cantidad y detalle de citas por día.
- **Administración:** registro de tratamientos y consulta de la agenda.

## Base de datos

La versión más completa del sistema utiliza PostgreSQL y organiza la información en dos entidades principales:

- **Tratamientos:** título, descripción, imagen y duración estimada.
- **Citas:** datos de contacto del paciente, tratamiento, duración, fecha y hora.

Las imágenes de los tratamientos se guardan en el sistema de archivos, mientras que su nombre se conserva en la base de datos para mostrarlas en el catálogo.
