# Bases de datos temporales

En la LZ se peude tener el rol de encargado de bases temporales, el cual consiste en inicializar la instancia de la maquina donde seran montadas las tablas temproales y la mejora del script de creacion de tablas temporales.

## Proceso

1. Iniciar bases temporales
    - Iniciar instancia
https://grupobancolombia.visualstudio.com/Vicepresidencia%20Servicios%20de%20Tecnolog%C3%ADa/_build/results?buildId=2348089&view=results
    - ejecutar script
      
          $ cd /home/svchad02/temporalDatabases
          $ sh initDatabases.sh

2. modificar desarrollo:
    
    - Acceder por ssh al servidor donde esta el desarrollo de baes temporales
    
          $ ssh riportil.adm@10.104.91.74
    
    - modificar

          $ cd /home/riportil.adm/AW1003001_BigDataCompany_BdTemporales_Dllo/Content_EC2