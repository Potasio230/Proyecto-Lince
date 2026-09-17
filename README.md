# Lynx Track

## Descripción

**Lynx Track** es una aplicación móvil orientada a mejorar la coordinación de servicios turísticos entre conductores, guías y coordinadores.

El proyecto busca centralizar la información de los servicios asignados, permitiendo consultar servicios, confirmar o rechazar asignaciones,
registrar disponibilidad y realizar el seguimiento del estado de los servicios.

## Identidad visual

### Logo

El logotipo de Lynx Track representa la esencia del proyecto. El lince simboliza agilidad, visión y adaptabilidad,
mientras que las montañas representan el turismo en Chile y la conexión con la naturaleza.

El logo se encuentra en:

```text
docs/diseno/logo.png
```

### Paleta de colores

| Color      | HEX       | Uso                                      |
| ---------- | --------- | ---------------------------------------- |
| Principal  | `#133154` | Botones principales                      |
| Secundario | `#0F8CB3` | Elementos secundarios                    |
| Fondo      | `#FFFFFF` | Fondo general                            |
| Texto      | `#133154` | Textos principales                       |
| Adicional  | `#CF7B0F` | Acentos y estados que requieren atención |

## Flujo de usuario

El siguiente diagrama representa el flujo principal de Lynx Track:

```mermaid
flowchart TD
    A([Inicio]) --> B[Iniciar sesión]
    B --> C{¿Credenciales válidas?}

    C -- No --> D[Mostrar error]
    D --> B

    C -- Sí --> E[Seleccionar rol]
    E --> F{¿Rol?}

    F -- Driver / Guía --> G[Inicio]
    G --> H[Consultar servicios asignados]
    H --> I{¿Tiene servicios asignados?}

    I -- Sí --> J[Seleccionar servicio]
    J --> K[Ver detalle del servicio]
    K --> L{¿Aceptar asignación?}

    L -- Sí --> M[Confirmar asignación]
    M --> N[Registrar Check-in]
    N --> O[Realizar servicio]
    O --> P[Registrar Check-out]
    P --> Q([Fin])

    L -- No --> R[Rechazar asignación]
    R --> H

    I -- No --> S[Consultar disponibilidad]
    S --> G

    F -- Coordinador --> T[Panel de monitoreo]
    T --> U[Consultar estados y respuestas]
    U --> V{¿Requiere reasignación?}

    V -- Sí --> T
    V -- No --> Q
```

El diagrama UML también se encuentra en:

```text
docs/diseno/flujo-usuario-uml.png
```


## Interfaces principales

Las pantallas definidas para el MVP son las siguientes:

### Login
![Login](docs/diseno/interfaces/login.png)

### Inicio / Servicios asignados
![Inicio](docs/diseno/interfaces/inicio.png)

### Detalle del servicio
![Detalle del servicio](docs/diseno/interfaces/detalle_servicio.png)

### Disponibilidad
![Disponibilidad](docs/diseno/interfaces/disponibilidad.png)

### Confirmación/Rechazo
![Confirmación/Rechazo](docs/diseno/interfaces/confirmacion.png)

### Check-in
![Check-in](docs/diseno/interfaces/checkin.png)

### Alertas
![Alertas](docs/diseno/interfaces/alertas.png)

### Monitor Logístico
![Monitor Logístico](docs/diseno/interfaces/monitor_logistico.png)

## Integrantes

| Integrante      | Rol          |
|-----------------| ------------ |
| Benjamin Aguero | Frontend     |
| Luciano Garrido | Backend      |
| Raúl Ferrini    | Frontend Dev |
| Ignacio Salazar | Scrum Master |

## Tecnologías

* Android Studio
* Kotlin
* Jetpack Compose
* Material Design 3
* Mermaid

## Evidencia

La evidencia correspondiente a la Clase 2 se encuentra en:

```text
docs/evidencias/Clase02/
```

El documento corresponde a:

```text
Evidencia_Clase_02_Diseno_Lince_Track.docx
```

## Diseño

Los recursos de diseño del proyecto se encuentran en:

```text
docs/diseno/
```

Esta carpeta contiene el logotipo, el diagrama UML y las interfaces de la aplicación.
