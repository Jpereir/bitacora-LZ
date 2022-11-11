# Certificacion procesos productizar

## Certificacion Coordinadores:
el proceso de certificacion de coordinadores consiste en ejecutar los coordinadores y validar que se haya echo la transferencia de los datos de manera correcta.

- **Verificar informacion:**
    - El desarrollador debe hacernos entrega de la HU y el release de los coordinadores. La HU debe estar a nombre del certificador y debe haber un comentario en la HU que indique el cambio a certificacion.
     - vamos al commit y a la carpeta API/cfg y revisar los coordinadores.
- **Release:**
     
    - **Recepcion Equipo CER:** Verificamos la recepcion a certificacion agregando el siguiente comentario y luego damos en Resume.
            
          Se aprueba la recepción del despliegue on premise de productizar
    
    - **Deploy CER:** Dejamos que el stage se complete de manera automatica.
    - **Manual Test:**
        - Debemos verificar que los coordinadores se hayan desplegado de manera correcta en la ruta del ambiente de CER `/opt/gitDevops/AW1003001_ProductizarLaAnalitica/<ApiName>/API/cfg`.
        - Ejecutar los coordinadores usando el comando
          
              $ sudo su - svchad02
              $ cd /opt/gitDevops/AW1003001_ProductizarLaAnalitica/ProductizarPy3
              $ nohup python3 coordinator.py /opt/gitDevops/AW1003001_ProductizarLaAnalitica/<ApiName>/API/cfg/<coordinator-name>.json &

            Tener en cuenta que puede que sea necesario ejecutar `coordinatorV2.py` y no `coordinator.py`
        -  Verficar los resultados en el directorio  `/opt/gitDevops/AW1003001_ProductizarLaAnalitica/<ApiName>/TMP_FILES/logs`. Se deben tomar pantallazos delos logs ya que son las evidencias.
        - Generar `testplan`.
        - Generar `DoD`.
        - Resume y comentario de Evidencias VSTS



## Certificacion API:
Unos de los procesos de certificacion cuando se trabaja con HUs de API es la de certificar la salida a produccion del API. Es decir llevar a produccion la Imagen del API. Para ello vamos a requerir de la HU, el release y los testplans creados para las pruebas especializadas.
- **Tomar evidencias:** Entramos a los `acceptance test` que tiene el `release`, luego a `gradlew test`. Mirar que diga TEST PASSED y tomar pantallazo de eso, serian dos pantallazos. El de acceptance test cert, y acceptance test dev. Anexar eso a el testplan y listo, esas son las validaciones.
- **Crear DoD:**
- **Trabjar Release:** Comentar en Security E2E 
    
      Evidencia VSTS: XXXX
- Mandar a probar el DoD, entregar nuevamente al desarrollador.