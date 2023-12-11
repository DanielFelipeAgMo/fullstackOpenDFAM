sequenceDiagram
  participant Usuario
  participant SPA
  participant Servidor

  Note over Usuario: Usuario interactúa con la SPA

  Usuario ->> SPA: Abre la SPA de notas

  SPA ->> SPA: Carga la interfaz de usuario

  Note over Usuario, SPA: Usuario crea una nueva nota

  Usuario ->> SPA: Escribe texto en el campo de texto

  SPA ->> SPA: Actualiza la interfaz con el texto ingresado

  Usuario ->> SPA: Hace clic en el botón "Guardar"

  SPA ->> Servidor: Envía la solicitud para guardar la nota

  Servidor -->> Servidor: Procesa y guarda la nota en la base de datos

  Servidor -->> SPA: Confirma la operación de guardado

  SPA -->> SPA: Actualiza la interfaz con la nueva nota

  Note over SPA: SPA puede cargar la lista actualizada de notas

  SPA ->> SPA: Solicita y carga las notas actualizadas

  Note over SPA: (Operaciones adicionales según la interacción del usuario)
