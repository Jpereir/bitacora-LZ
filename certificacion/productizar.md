# Productizar
## Certificacion Coordinadores
## Certificacion API:
Unos de los procesos de certificacion cuando se trabaja con HUs de API es la de certificar la salida a produccion del API. Es decir llevar a produccion la Imagen del API. Para ello vamos a requerir de la HU, el release y los testplans creados para las pruebas especializadas.
- **Tomar evidencias:** Entramos a los `acceptance test` que tiene el `release`, luego a `gradlew test`. Mirar que diga TEST PASSED y tomar pantallazo de eso, serian dos pantallazos. El de acceptance test cert, y acceptance test dev. Anexar eso a el testplan y listo, esas son las validaciones.
- **Crear DoD:**
- **Trabjar Release:** Comentar en Security E2E 
    
      Evidencia VSTS: XXXX
- Mandar a probar el DoD, entregar nuevamente al desarrollador.