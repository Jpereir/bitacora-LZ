# Refinamiento Rutinas:
- **last_update:** 2022-06-15

## Documentacion
- La documentacion del proceso de ingestiones puede ser encontrado en la seccion de [rutinas](../rutinas/README.md) de la presetente documentacion.

## Checklist

## Proceso
En los refinamientos de `Historias de Usuario` de rutinas el objetivo es determinar que la informacion brindada por el usuario es suficiente para poder trabajar la HU. El proceso de refinamiento se lleva a cabo de la siguiente manera:

- **Leer la historia de usuario:** Se debe leer la HU y los distintos comentarios que haya para obtener el contexto de la misma. Debemos verificar qué informacion nos da el usuario respecto al repositorio y pull-request de la rutina que se trabajar, tambien debemos asegurarnos que la HU cuente con un padre.
- **Verificar tipo de HU:**
si es una rutina tradicional o virtual. las tradicionales entregan codigo compleoto, las virtuqales entrgan pr. 
si es revision
si es modificacion
si es calendarizacion


- **Identificar datos:**
en algunas ocacuioens entregan docuemntacion

verificar cantidad de logs, almenos 10 logs, los logs con ejecucion exitosa
verificar que no hayan errores, algunos errores son tolerables. que los logs sean de almenos 3 dias y que hayan 2 horas entre ellos. esto se puede verificar con el nombre de los logs ya que el nombre es la fecha y la hora de ejecucion.

verificar que los lofs son despues del pr.
nota, esto esta en veremos, por ahi hay un comenario
Estos lineamientos de los dias y las horas es para que se tomen distintos posibles escenarios

los logs en las rutinas tradicionales vienen dentro del codigo.


verificar pull request si se trata de rutionas virtuales o el codigo si se trata de tradicionales.
Si entregan el repositorio buscar en los pr de  dicho repo al usiaro, el pr debe estar activo y listo para aprobar, echarle un ojo por encima de los archivos del pr, verificar como minimo el config que tenga el dsn bien.

verificar prefijo de repo
verificar que vaya de master a trunk

verificar grupo USD, hace parte de la documentacion y hace parte del proceso del seguimiento de rutinas, tambien es para saber a que area se pasan las incidencias

si no estoy mal en la wikti tambien se debe poner esto del grupo usd.


nota la idea es que ya no llegue rutinas tradicionales, solo rutinas virtuales, quedaran alguna que otra tradicional que sea modificacion

HAcer comentario en la HU.

si es calendarizacion veriicar la hora y la periodicidad
- En el setup.py esta especiicado que orquestador se usa.


# TO-DO
Pull request del HU
Leer los comentarios de la HU
revisar logs
- revisar el prefijo del repositorio


LISTA DE PREFIJOS

bana-

veg-

vcum-

vedp-

vrgo-

vspc-

vitd-

vsas-

vpyp-

vnc-

vsuf-

veyg-

vmdo-