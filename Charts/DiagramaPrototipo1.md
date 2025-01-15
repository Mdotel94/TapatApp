```mermaid
flowchart TD
    A[Client View<br>Input username] --> B[Client DAO User<br>getUserByUsername]
    B -->|Envia dades username| C[Petició HTTP<br>GET username]
    C --> D[Servidor<br>Webservice]
    D -->|Consulta DAOUser| E[Server DAO User<br>getUserByUsername]
    E -->|Respon Objecte User<br>if exists| D
    D -->|Reposta HTTP amb Json<br>User if exists| B
    B -->|Dades processades| F[Client View<br>Show Info User if exists]
