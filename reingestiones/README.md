- borrar avros
    - identificar avros a eliminar
    - mover avros a la carpeta trash
        -  crear subcarpetas para poder realziar restauraciones de ser posible
- ejecutar comando del tapa huecos en la ruta
    cd /home/svchad02/scripts/restauracion_fn_lz

    nohup ./restauracion.py -G"numMappers=4" restore --subdomain Seguridad_Gestion_Fraude_SQLServer_MINERIA -st CONSOLIDADO_ENUM -ss REGLAS_FILES -hv S_Apoyo_Corporativo -dta WEB -dts REGLAS_FILES -dt CONSOLI_ENUM -db SQLServer -iy 2022 -im 10 -id 19 --ignore-avros-in-target --split-by FECHA_ENUM --where "FECHA_ENUM > 20220901 and FECHA_ENUM <= 20221018" &

- cerrar la Hu:
    - Verificar el archivo Documetnacion por tipoligia de Hu - cierra en la carpeta de gestion de historias de usuario donde esta la info de que cosas se deben agregar en le cierre de la HU