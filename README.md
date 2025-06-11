flowchart TD
    A[Inicio de la App] --> B{¿Usuario ha iniciado sesión?}
    B -- Sí --> C[Ir al Inicio]
    B -- No --> D[Pantalla de Inicio de Sesión / Registro]
    D --> E{¿Inicio exitoso?}
    E -- Sí --> C
    E -- No --> F[Mostrar error de autenticación]

    C --> G[Explorar por categorías]
    C --> H[Buscar cómic]
    C --> I[Ver cómics guardados]
    C --> J[Acceder a perfil / ajustes]

    G --> G1[Seleccionar categoría]
    G1 --> G2[Ver lista de cómics]
    G2 --> G3[Seleccionar cómic]

    H --> H1[Escribir búsqueda]
    H1 --> H2[Ver resultados]
    H2 --> H3[Seleccionar cómic]

    G3 --> K[Ver detalles del cómic]
    H3 --> K

    K --> L{¿Leer ahora?}
    L -- Sí --> M[Pantalla de lectura de cómic]
    L -- No --> N[Volver a lista o guardar en favoritos]

    M --> O[Leer página por página]
    O --> P{¿Cómic terminado?}
    P -- Sí --> Q[Recomendar cómics similares]
    P -- No --> O

    J --> J1[Editar perfil]
    J --> J2[Ver suscripción]
    J --> J3[Cerrar sesión]
    J3 --> A

