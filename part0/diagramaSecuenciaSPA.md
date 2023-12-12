sequenceDiagram
  participant Usuario
  participant Navegador
  participant SPA

  Note over Navegador: Usuario ingresa a la SPA

  Usuario ->> Navegador: Ingresa a https://studies.cs.helsinki.fi/exampleapp/spa

  Navegador ->> SPA: Solicita la SPA de notas

  SPA -->> Navegador: Devuelve la SPA de notas

  Navegador -->> Usuario: Carga la SPA en el navegador

  Note over Usuario, SPA: Usuario interactúa con la SPA

  Usuario ->> SPA: Explora la SPA de notas

  Note over SPA: SPA carga dinámicamente las notas

  SPA ->> SPA: Solicita y carga las notas

  Note over Usuario, SPA: Usuario crea una nueva nota

  Usuario ->> SPA: Escribe texto en el campo de texto

  SPA ->> SPA: Actualiza la interfaz con el texto ingresado

  Usuario ->> SPA: Hace clic en el botón "Guardar"

  SPA ->> SPA: Envía la solicitud para guardar la nota

  SPA -->> SPA: Guarda la nota localmente

  Note over SPA: Actualiza dinámicamente la lista de notas

  SPA -->> Usuario: Muestra mensaje de éxito o fallo

  Note over Usuario, SPA: Usuario explora más la SPA

  Note over SPA: SPA maneja las interacciones del usuario

  Note over SPA: (Operaciones adicionales según la interacción del usuario)
