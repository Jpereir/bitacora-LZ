# Checklist Ingestiones
- last_update: 2022-06-07

0. Crear tareas VSTS.
1. Revisar HU.
2. Preparar datos
3. Preparar repositorio.
4. Generar tablas temporales.   
    1. Iniciar Servidor.
    2. Creación de tablas.
        - Obtener metadata.
        - Guardar medatada.
        - Crear tabla.
    3. Ajustar configs y passwords.
        - Backup archivos.
        - Agregar config.
    4. Modificar Eval.   
5. Generar y executar paquete. 
    - Copiar la plantilla
    - Ejecutar el script.
    - Verificar output
    - Mover paquete.
    - Ejecutar paquete     
6. Revisar ejecuicion del paquete.
    - Revisar fuente. 
    - Revisar LZ.
7. Automatizacion de certificacion.
    - Crear lista de flujos.
    - Ejecutar pruebas
    - Verificar resultados.
8. Cerrar desarrollo.
    - Mover plantilla.
    - Mover a workflows.
    - Crear archivo .ini.
        - creacion auto_exe.ini.
        - creacion manual_exe.ini.
    - Push a trunk. 
    - Crear pull-request.
9. Trabajar realese. 
    - Deploy DEV.
    - Acceptance Test DEV.
    - Reception HU Equipo.   
    - Deploy CER
    - Manual Step Execution.
    - Acceptance Test UAT.
    - Aprovacion certificacion.
    - Pre-validacion
        - Determinar el nombre del proceso.
        - Matriz de riesgo.
        - WikiTI.
        - DoD.
        - Test plan.
        - Verificacar datos.
            - Validación PMO titulo DOD
            - Validación HU titulo DOD
            - Validación padre del DOD
            - Validación related DOD
            - Validación trunk DOD
            - Validación Pipeline DOD
            - Validación test plan numero en DOD
            - Validación ruta documentación
            - Validación célula DoD
            - Validación sprint DoD
            - Validación historia DOD
            - Validación Aprobado DoD
            - Validación numero de caracteres criterios de aceptación HU
            - Validar que haya una tarea activa
            - Validación PMO titulo test plan
            - Validación HU titulo test plan
            - Validación Sprint título test plan
            - Validación célula Test plan
            - Validación Sprint Test Plan
            - Validación descripción test plan release
            - Validación descripción test plan Título HU
            - Validación adjuntos test plan
            - Validación padre test plan igual que padre HU
            - Validación test plan con HU relacionada
            - Validación test plan CERRADO
            - Validación cambio de variables en release
            - Validación release documentado
        - Deploy.        
    - Create OC.
    - Deploy PDN.
    - Execute Auto Inventor
    - Execute Manual Commands PDN
    - User Validation




        
    

