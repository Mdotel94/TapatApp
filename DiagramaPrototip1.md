flowchart TD
    A[<b>Client View</b> <br> Input username] -->|Envia dades username| B[Client DAO User<br> getUserByUsername]
    B -->|Petición HTTP  GET username| C[<b>Servidor</b> <br> Webservice]
    B -->|Resposta HTTP amb Json User if exists| C[Client DAO User<br> getUserByUsername]