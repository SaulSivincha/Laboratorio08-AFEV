# Ejercicio 3 — Control de acceso

El archivo `login_model.smv` verifica las siguientes propiedades CTL:

```smv
SPEC AG (!input_valid -> !logged_in)
SPEC AG (input_valid -> AF logged_in)
```

Ejecuta:

```bash
NuSMV Ejercicio3/login_model.smv
```

Ambas propiedades se verifican como `true`.
