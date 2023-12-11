sequenceDiagram
    participant Usuario
    participant Navegador
        participant Servidor

  Note over Navegador, Servidor: Usuario abre la página

  Usuario ->>+ Navegador: Ingresa a https://studies.cs.helsinki.fi/exampleapp/notes

  Navegador ->>+ Servidor: Solicita la página de notas

  Servidor -->>- Navegador: Devuelve la página de notas

  Note over Usuario, Navegador: Usuario escribe una nueva nota

  Usuario ->>+ Navegador: Escribe texto en el campo de texto

  Note over Navegador: Usuario interactúa con la interfaz

  Navegador ->>+ Navegador: Actualiza la interfaz con el texto ingresado

  Note over Usuario, Navegador: Usuario hace clic en el botón "Guardar"

  Navegador ->>+ Servidor: Envia la solicitud para guardar la nota

  Servidor -->>- Navegador: Guarda la nota en la base de datos

  Navegador -->>+ Usuario: Muestra mensaje de éxito o fallo

  Note over Navegador, Servidor: Actualiza la interfaz con la nueva nota

  Navegador ->>+ Servidor: Solicita la lista actualizada de notas

  Servidor -->>- Navegador: Devuelve la lista actualizada de notas

  Note over Navegador: Actualiza la interfaz con las notas actualizadas
