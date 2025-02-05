# By-More-Doc
### ***¿Que es exactamente By-More-Doc?*** 

By-More-Doc es una aplicacion movil que nacio con la idea de hacer que aquel que quiera información documentada o simplemente saciar su curiosidad tenga un lugar donde compartir absolutamente todo aquello que crea que pueda interesarle a alguien o que quieran encontrar documentos concretos.
***
***<h1> Objetivos de la aplicación</h1>***

- Romper la privatización y compra venta de información 
- Juntar a fanaticos de todos los tipos
- Facilitar el acceso a documentos
- Compartir la información
- Incitar la colaboración
 ***

 |<u> Apartados<u> | Disponible | Ultima actualización |
|----------------|------------|----------------|
| App           | <p style="color:green;">Sí</p>         |<center>30/1/2025</center> |
| BD            | <p style="color:green;">Sí</p>|<center>30/1/2025 </center>|
| Contactos     | <p style="color:green;">Sí</p>|<center>30/1/2025 </center>|
| Pagina web    | <p style="color:red;">No </p>||

``` mermaid 

journey
    title Como avanza Los apartados
    section Selección de productos
        App: 6
        BD: 6
        Contactos: 6
        Pagina web: 1

```


``` mermaid 
pie
    title Apartados disponibles
    "Disponible": 75
    "No Disponible": 25
```

[Un video para repasar conceptos](https://www.youtube.com/watch?v=U709qY6S9rA&list=PLU8oAlHdN5BktAXdEVCLUYzvDyqRQJ2lk&index=1)

[![Un video para repasar conceptos](https://img.youtube.com/vi/U709qY6S9rA/0.jpg)](https://www.youtube.com/watch?v=U709qY6S9rA&list=PLU8oAlHdN5BktAXdEVCLUYzvDyqRQJ2lk&index=1)



***<h1>Creación De Usuario</h1>***


``` mermaid 



graph TD
    A[Inicio] --> B{Escribe tu contraseña}
    B --> C((pass))
    C --> D{¿Contraseña correcta?}
    D -- Sí --> E[Login correcto]
    D -- No --> F[Intentar de nuevo]
    F --> B
    A --> G{Crear usuario}
    G --> H((pass))
    H --> I{¿Existe ya unos datos asi?} 
    I -- Sí --> G
    I -- No --> J{Creamos usuario}
    J --> A




```
``` mermaid 

sequenceDiagram
actor User as Usuario
participant FE as Frontend
participant BE as Backend
participant DB as Base de Datos

User ->> FE: Envío de datos
FE ->> BE: Validación de datos
BE ->> DB: Verificar existencia
DB -->> BE: Datos Unicos Exixtentes
BE -->> FE: Respuesta validada
FE -->> User: Cuenta Creada

```

***<h1>Creación De Documentos (tablas)</h1>***

``` mermaid 

erDiagram
    RESPALDO {
        string id_respaldo
        string nombre
        String texto
    }
    USUARIO {
        string id_usuario
        string nombre
        string Telefono
    }
    DOCUMENTO {
        string id_Documento
        string id_usuario
        string id_respaldo
        string texto
    }
    USUARIO ||--o{ DOCUMENTO : "Crea"
    RESPALDO }o--|| DOCUMENTO : "Contiene"

```
***<h1>Diagrama Git (Panificación)</h1>***

``` mermaid 
gitGraph
    
    commit id: "Configuración inicial"
    
    branch dev
    commit id: "Añadimos la primera conf"
    
    checkout main
    commit id: "Creamos la APP"
    merge dev
    checkout dev

    commit id: "Agregamos la BD"

    commit id: "Comprobar el funcionamiento"
    checkout main
    commit id: "Vinculamos la App con la DB"

    merge dev


    branch bugfix
    
    checkout main
    commit id: "Versión 1.0.0"tag: "Versión 1.0.0"
```

``` mermaid 
gantt
    title Diagrama de Gantt
    dateFormat DD-MM-YYYY
    section APP
        Creación         :a1, 27-03-2025, 30d
        Usuarios    :a2,after a1, 20d
        Puesta en marcha    :after a2, 20d
    section DB
        Creación y conf : 27-03-2025, 30d
        Vincular App    :4d
        Añadir datos usuarios :16d

```

***<h1>Minimos funcionalidad</h1>***


```mermaid
graph TD;
    A[Requerimientos del Sistema] -->|Funcional| B[Autenticación de Usuario]
    A -->|Funcional| C[Gestión de Documentos]
    A -->|No Funcional| D[DB]
    A -->|No Funcional| E[Rendimiento]

    B -->|Debe permitir| B1[Inicio de sesión]
    B -->|Debe permitir| B2[Registro de usuario]
    B -->|Debe permitir| B3[Recuperación de contraseña]

    C -->|Debe incluir| C1[Agregar Documento]
    C -->|Debe incluir| C2[Editar Documento]
    C -->|Debe incluir| C3[Eliminar Documento]

    D -->|Debe cumplir| D1[Cifrado de datos]
    D -->|Debe cumplir| D2[Autorización basada en roles]

    E -->|Debe garantizar| E1[Tiempos de respuesta cortos]
    E -->|Debe soportar| E2[Escalabilidad]
    
    %% Personalización con estilos
    classDef titulo fill:#004466,stroke:#ffffff,stroke-width:2px,font-size:14px,color:#ffffff;
    classDef funcional fill:#0099cc,stroke:#005577,stroke-width:2px,font-size:12px,color:#ffffff;
    classDef noFuncional fill:#ff9933,stroke:#cc6600,stroke-width:2px,font-size:12px,color:#ffffff;
    classDef subRequerimiento fill:#ffffff,stroke:#666666,stroke-width:1px,font-size:11px,color:#000000;

    class A titulo;
    class B,C funcional;
    class D,E noFuncional;
    class B1,B2,B3,C1,C2,C3,D1,D2,E1,E2 subRequerimiento;

``` 

***<h1>Contactos</h1>***

<marcos.lasheras.trzn@gmail.com>

 


![Seguidores en GitHub](https://img.shields.io/github/followers/marcos-trzn?style=social)
