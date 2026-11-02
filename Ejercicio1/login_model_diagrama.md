# Modelo de transición: inicio de sesión

```mermaid
stateDiagram-v2
  [*] --> SinCredenciales: input_valid = FALSE\nlogged_in = FALSE
  SinCredenciales --> CredencialesValidas: siguiente ciclo
  CredencialesValidas: input_valid = TRUE\nlogged_in = TRUE
  CredencialesValidas --> SinCredenciales: siguiente ciclo
```

La corrección se basa en mantener `logged_in = input_valid` en cada estado alcanzable.

Propiedades verificadas:

```smv
SPEC AG (!input_valid -> !logged_in)
SPEC AG (input_valid -> AF logged_in)
```


