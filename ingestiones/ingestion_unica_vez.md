# Ingestion una unica vez.

Son ingestiones que solo se deben hacer una vez en PRD por ende no tienen una periodicidad para regsitrar en malla. Este tipo de ingestiones se llevan acabo sin release ni requieren de un paquete de ejecucion, ya que como se menciono, la ingestion se hace una unica vez. La ingestrion se hace utilizando un script directamente en produccion. Sin embargo se aconseja primero hacer pruebas en el entorno de desarrollo.

El script que se usara es el denominado tapa huecos con el que tambien se realizan reingestiones. En esta ocacion dicho script sera utilizado con el parametro `historical`.

## Proceso:
- **Crear tarea**
- **Revisar HU:** En la HU debe estar explicito que se trata de una ingestion de una unica vez.
- **Preparar comando.** El script a utilizar para la ingestion unica es el siguiente. Este comando se debe ejecutar para cada una de las tablas solicitadas.
            
       $ nohup ./restauracion.py historical -st <source_table_name> -ss <source_schema> -sb <subdominio> -db <motor_db> -hv <db_hive> -iy <current_year> -im <current_month> -id <current_day> --split-by "<coulmn_split>" -dta <aplicativo> -dts <dst_schema> -dt <dst_table_name> --ignore-avros-in-target --partitioned-by YEAR &

    Para ello necesitaremos una serie de datos que podremos sacar de la plantilla compartida pro el usuario.

        <source_table_name>
        <source_schema>
        <subdominio>
        <motor_db>
        <db_hive>
        <current_year>
        <current_month>
        <current_day>
        <coulmn_split>
        <aplicativo>
        <dst_schema>
        <dst_table_name>

- hacer conteos 
- hacer metadata

- **Pruebas en desarrollo.** [**PROCESO PROBADO SIN EXITO**]
Para entender mejor el tema de ingestiones de una unica vez y para detectar algun tipo de error se recomienda primero realziar pruebas en el entorno de desarrollo usando  bases de datos temporales.
    - **Montar tablas temporales:** Se deben montar las tablas temporales para las tablas solicitadas en la historia de usuario. El proceso esta descrito en la guia de ingestiones.

        A lo mejor hay que crear el subdominio para pdoer ejecutar el eval.


   
        
    - **Ejecutar script**
    nos dirijimos a la ruta /home/svchad02/scripts/restauracion_fn_lz que es donde se encuentra el script que vamos a ejecutar. alli ejecutamos el comando luego de haberlo preparado con los datos de la HU.

    - **Revisar  resultados ingestion**
- **Ejecucion en produccion.**

    - **Abrir asistente:** Nos dirigimos al asistente web a la seccion de ejecutar programa del menu Servicios.

ejecutar programada
    cd /home.....
    nohup
    executar
    ir a hue prd
    comprar numero de registros

verificar conexion a tavlas de la lz
cometnar HU

hacer un cometnario donde se muestre la evidencia  de los conteos de un lado y del otro y que la ingestion quedo en verdesito.
    