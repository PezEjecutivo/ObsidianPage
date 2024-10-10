
Se pueden realizar diferentes esquemas aunque es un poco complejo, aunque podemos hacerlo a mano, si es un esquema de algo que ya esta hecho, la mejor opción que tendremos es pasarle una plantilla base a una IA y pedirle a esta que te genere el esquema que quieres siguiendo esa plantilla.

Aunque parezcan imágenes, están hechos con texto plano.
## Diagrama de secuencia
```mermaid
sequenceDiagram
  autonumber
  Client->>Server: Send data
  Note right of Server: No handshake or acknowledgment
  Client->>Server: Send more data
  Note right of Server: Unreliable, no delivery guarantee

```

## Diagrama de estados
```mermaid
stateDiagram-v2
  state fork_state <<fork>>
  [*] --> fork_state
  fork_state --> Detección_Anomalías : Análisis de tráfico
  fork_state --> Detección_Firmas : Comparación con firmas conocidas

  state join_state <<join>>
  Detección_Anomalías --> join_state
  Detección_Firmas --> join_state
  join_state --> Respuesta_Incidente : Generar alerta / Acciones correctivas
  Respuesta_Incidente --> [*]

```

Hay diagramas de clases y relacionales, pero al estar más relacionados directamente con bases de datos no los voy a añadir, pero desde este enlace puedes ver la documentacion de la plantilla [Más tablas](https://squidfunk.github.io/mkdocs-material/reference/diagrams/#using-flowcharts "Como poner más tablas").