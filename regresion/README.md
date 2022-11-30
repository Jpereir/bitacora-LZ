# Regresion

Modificaciones en los paquetes getContext que no afecten la logica de ingestiones en produccion. En estos proceso entran. Esto con el objetivo de no hacer un reproceso ejecuando pruebas.
- HU de depuracion:
- Sacar un flujo de un paquete:
    - El paquete viejo no es necesario reetestearlo. En este caso se ejecutan ambos ambos paquete pero solo se le hacen pruebas automatizadas al paquete nuevo. Es decir las evidencias solamente las llevaria el paquete nuevo.
- Cambiar el numero de mappers:
    - Como desarrollador de la HU: Es necesario hacer una ejecucion del paquete pero sin las pruebas del automatizadas. Por ende en el pr solo irian los cambuios del paquete, sin .ini ni workflow, es decir, no se haria prueba controlada en PRD.
    - Como certificador: no es necesario ejecutar paquete ni realziar pruebas automatizadas.

Modificaciones que no entran en regresion.
- Cambiar la semilla.

