# Ejercicios parte0

    sequenceDiagram
        participant browser
        participant server

        browser->>server: Envío de nota de formulario por POST https://studies.cs.helsinki.fi/exampleapp/new_note
        server->>browser: Servidor envia HTTP 302 para reenviar la nota por GET a la direccion /exampleapp/notes
        browser->>server: Se envía la nota del formulario por GET a /exampleapp/notes
        server->>browser: Se envía codigo HTTP 200 y el archivo data.json para renderizarlo en el browser.



    sequenceDiagram
        participant browser
        participant server

        browser->>server: Envío de petición de la pagina spa por metodo GET https://studies.cs.helsinki.fi/exampleapp/spa
        server->>browser: Servidor envía codigo HTTP 200 y se recargan los archivos main.css, spa.js y data.json.

    sequenceDiagram
        participant browser
        participant server

        browser->>server: Envío de nueva nota por POST a studies.cs.helsinki.fi/exampleapp/new_note_spa
        server->>browser: Servidor devuelve codigo HTTL 201Created con la respuesta  message:"note created"
