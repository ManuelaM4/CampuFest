CampusFest es una plataforma para gestionar la reserva de cupos en eventos universitarios: conciertos, torneos de videojuegos, encuentros deportivos y actividades culturales. Los estudiantes consultan eventos y reservan cupos (que deben confirmar en máximo 10minutos); los organizadores administran la información y generan reportes. Cada evento tiene un aforo máximo. Los cupos bloqueados para organización no pueden reservarse. Cada reserva Confirmada ocupa un cupo. Una reserva Pendiente vigente también ocupa un cupo provisional. Una reserva Pendiente vence 10 minutos después de su creación si no se confirma. Al vencer, deja de ocupar cupo. Las reservas Canceladas y Vencidas no ocupan cupo. El sistema no debe aceptar reservas que superen el aforo. Solo reservas Confirmadas pueden registrar ingreso mediante un código QR válido; un ingreso se registra una vez. Toda edición de un evento registra la fecha y hora de la última modificación.

## Descripción del sistema

Los estudiantes consultan eventos y reservan cupos, que deben confirmar en máximo 10 minutos. Los organizadores administran los eventos y generan reportes. Reglas de negocio que gobiernan el modelo:

- Cada evento tiene un **aforo máximo**, y los cupos **bloqueados** para la organización no se pueden reservar.
- Una reserva **Confirmada** ocupa un cupo; una **Pendiente** vigente ocupa un cupo provisional.
- Una reserva Pendiente **vence 10 minutos** después de crearse si no se confirma, y al vencer deja de ocupar cupo.
- Las reservas **Canceladas** y **Vencidas** no ocupan cupo.
- El sistema **no acepta reservas que superen el aforo**.
- Solo las reservas Confirmadas pueden **registrar ingreso con un código QR válido**, y el ingreso se registra una sola vez.
- Toda edición de un evento registra la **fecha y hora de la última modificación**.

## Casos de uso

Actores: **Estudiante**, **Organizador** y el **Reloj** (10 minutos de una reserva), que dispara la cancelación por vencimiento. Todos los casos incluyen `Consultar eventos`.

## Clases de análisis

| Tipo | Clases |
| --- | --- |
| **Límite** (interacción con el actor) | `PantallaEvento`, `ReporteReservas`, `ReporteAsistencia` |
| **Control** (lógica y cálculos) | `GestionEvento`, `GestionReserva`, `GestionAsistencia`, `CalculoDispCupos` |
| **Entidad** (información persistente) | `Evento`, `Reserva`, `Asistencia`, `Estudiante` |
