# Ejercicio 2 — Ejecución interactiva de `intro-demo.smv`

Inicia NuSMV en modo interactivo desde el directorio raíz del repositorio:

```bash
NuSMV -int Ejercicio1/intro-demo.smv
```

En el intérprete ejecuta, en este orden:

```text
read_model -i Ejercicio1/intro-demo.smv
flatten_hierarchy
encode_variables
build_model
pick_state -i
simulate -i -k 10
```

`pick_state -i` muestra el estado inicial esperado: `location = l1` y `x = 0`. Con `simulate -i -k 10`, presiona Enter para avanzar y observar las transiciones entre `l1` y `l2`.
