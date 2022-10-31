# Landing zone 
**last_update:** 2022-05-27

Documentacion de los distintos procesos de se realizan en la LZ (Landing zone), la cual esta encargada de la gestion de la data del banco, la cual esta almacenada en un HDFS. Para la fecha se esta trabajando en migrar de este HDFS local (On-Premise) a servidores publicos de Cloudera (CDP).

- **Refinamiento:** Proceso donde se verifican las Historias de Usuario (HU) que se trabajaran en el siguiente spring. A grandes rasgos hay que verificar la existencia, acceso, permisos de las tablas mencionadas en la HU.

- **Ingestiones:** Proceso de transferencia datos desde bases de datos de usuarios (diferentes secciones del Banco) al HDFS a traves de sqoop. En este proceso se genera un script que realizara la transferencia de los datos con cierta peridiosidad definida. Para mayor informacion revisar la [documentacion de ingestiones](./ingestiones.md). Para realziar ingestiones es necesario contar con una copia del repositorio [AW1003001_BigDataCompany](https://grupobancolombia.visualstudio.com/Vicepresidencia%20Servicios%20de%20Tecnolog%C3%ADa/_git/AW1003001_BigDataCompany), el repositorio debe ser clonado con el usuario `svchad02`.

      $ sudo su - svchad02
      $ git clone <repo-location>

    Antes de realziar algun commit configurar el email en git para evitar problemas al realizar algun pull request.

      $ git config --global user.email "<bancolombia-user-email>"

- **Reingestiones:** Proceso donde se hace la ingesta de una porsion de una tabla. Por distintas razones el proceso de ingesta en produccion puede vayar para uno o varios periodos, horas, dias, etc, cuando esto sucede, los usuarios solicitan a la LZ borrar y volver a cargar los periodos con errores o vacios que se tengan en las bases de datos de la LZ. En resumidas cuentas consiste en tapar los huecos de datos existentes en las bases de datos.

- **Soporte estructural:** Consiste en desarrollos para el mejoramiento de los procesos de la Lz.

### Glosario:
- **Subdominio:** Archivo de configuracion para realziar la conexion a una base de datos.

### Tips sprints
- Se pueden solicitar puntos para autoaprendizaje.
- Las tareas deberian estar abiertas por 4 a 8 horas.
- Certificacion = UAT = QA
- Las HU deberian durar un solo sprint. Deben ser tareas que se logren en un solo sprint.
- Se puede solicitar puntos para preparar los learning days.

### Algunos comandos utiles

Si sale algun error en ambientes pre-productivos con el mensaje Client cannot authenticate via:[TOKEN, KERBEROS]
  $ kinit svchad02@AMBIENTESBC.LAB -k -t /opt/cloudera/security/keytabs/svchad02.keytab

Matar un proceso en hue dev
oozie job -oozie https://$STR_CNX_OOZIE -kill <ID_HUE>