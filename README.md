# ControlPadrones
Control de Padron SAP con padrones de ARBA y CABA
---
De: Marina Mariel Chavez 
Enviado el: jueves, 6 de enero de 2022 14:59
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Buenísimo!

Ahora sí, entonces para poder programar debería poner nombre a los padrones y armar dos listas para ambos padrones?

Marina
---
De: Miguel Angel Cabrera 
Enviado el: jueves, 6 de enero de 2022 15:32
Para: Marina Mariel Chavez <marina.chavez@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola, ok

Te paso como quedaría si tiene Alicuota lo trae y si no lo deja vacío.

Miguel Angel Cabrera
Auditoria interna
Tel: (54) 0362-4456000 - Interno 3820
---
De: Marina Mariel Chavez 
Enviado el: jueves, 6 de enero de 2022 14:59
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola Migue,

Recién pude hacer un control del cruce que hiciste.

Hay algo nada más que habría que ver, y es el caso de los proveedores que no están en el padrón, ya sea de ARBA o CABA, no debería traer alícuota 0 debería traer el campo vacío, porque a los que tienen alícuota 0 se les asigna el indicador que corresponde y a los que no están no se les carga indicador alguno.

Te paso dos casos:

CABA (Cruce mío)
 

CABA (Cruce Miguel)
 

Bs. As. (Cruce mío)
 

Bs. As. (Cruce Miguel)
 

Se podrá hacer algo para que no traiga 0?


Marina Mariel Chavez
Impuestos
Predio 404 - Ruta N. Avellaneda Km. 15,5 
(3500) Resistencia-Chaco
Tel: (54) 0362 – 4456 000 int.3022
marina.chavez@grupocarsa.com
---
De: Miguel Angel Cabrera 
Enviado el: miércoles, 5 de enero de 2022 10:29
Para: Marina Mariel Chavez <marina.chavez@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola, buen día

Ok, te paso como quedaría el archivo. Lo hice con ACL porque a la compu que tengo no le da para hacerlo con Excel, pero se puede hacer si tenes una maquina con mas recursos.

Lo dejé en la carpeta //ACL/Control
En la carpeta //ACL/Control/Archivos están los archivos que necesito para comparar, el de proveedores SAP, PadronRGS (lo tomo como ARBA) y RG (lo tomo como CABA). 
Para la alícuota que muestro estoy tomando la columna 9 de ambos padrones.

Esto lo puedo programar en automático, tendrías que dejar ambos padrones actualizados con un nombre determinado en alguna carpeta para que el programa los levante y genere.

Saludos.

Miguel Angel Cabrera
Auditoria interna
Tel: (54) 0362-4456000 - Interno 3820
---
De: Marina Mariel Chavez 
Enviado el: miércoles, 5 de enero de 2022 06:43
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP



Hola Migue, buen día!

En esa planilla está todo lo que yo hago, pero solamente necesito cruzar la hoja 4, que es donde están todos los proveedores de SAP con su número de proveedor y CUIT con el padrón, ya sea de ARBA o CABA, y que el cruce me traiga la alícuota que tenga, en caso de que corresponda tenga alícuota, hay muchos que no están en los padrones y queda vacía la celda.

De lo demás me encargo yo, es sencillo lo que necesito, pasa que para no tener tantas planillas yo le pasaba a Diego mi planilla de trabajo y él ya sabía que hoja utilizar.

Marina
---
De: Miguel Angel Cabrera 
Enviado el: martes, 4 de enero de 2022 17:11
Para: Marina Mariel Chavez <marina.chavez@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

A ver si entiendo, vos necesitas armar la hoja CONTROL? Estoy mirando solo ARBA por ahora.

Hasta ahora veo que lo podemos armar con Excel (igual después quizás lo termine armando con ACL, pero me sirve para entender),

Estoy pensando tener varios archivos:

1.	Indicadores: Hoja Indicadores
2.	IndicSAP_ARBA: Hoja Indic SAP después - ARBA
3.	CUIT_ Hoja CUIT
4.	Padrón: Esto supongo que sería el archivo (PadronRGSRet012022.txt), veo que la hoja Padrón parte 1 no tiene ninguna alícuota cargada (eso está ok?).

Supongo que como resultado solo te interesa las diferencias.

Coméntame si estas hojas la armas vos y si es fácil obtener, porque excepto el padrón podemos sacar directamente de SAP.

 

Saludos.

Miguel Angel Cabrera
Auditoria interna
Tel: (54) 0362-4456000 - Interno 3820
---
De: Marina Mariel Chavez 
Enviado el: martes, 4 de enero de 2022 10:16
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Me olvide de comentarte que el padrón de CABA tiene las alícuotas de percepción y las de retención, la columna 9 está la alícuota de retención:

23122021;01012022;31012022;20000163989;D;S;N;0,00;0,00;00;00;

Si bien estoy tramitando la baja como agente en CABA, hasta que no nos den de baja tenemos que continuar reteniendo, con lo cual tengo que seguir subiendo los padrones y controlando que se asignen las alícuotas correctas a los proveedores.

Marina
---
De: Marina Mariel Chavez 
Enviado el: martes, 4 de enero de 2022 9:57
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola Migue,

Es así como indicas, algo similar a un buscarv.

Los archivos que cruzo hoy son: padrones de Bs As (PadronRGSRet012022) y el de CABA (RG), que cruzo con las planillas que te dejo en la carpeta que dice ACL porque no puedo mandar por correo.

Planilla Control Arba (cruce con última hoja) y lo mismo para la de Control CABA.

De las opciones que me pasaste dejaría trabajar con BI como última, me parece que la 3er opción es la más viable.

Avisame si no me explico bien. 

Marina Mariel Chavez
Impuestos
Predio 404 - Ruta N. Avellaneda Km. 15,5 
(3500) Resistencia-Chaco
Tel: (54) 0362 – 4456 000 int.3022
marina.chavez@grupocarsa.com
--- 
De: Miguel Angel Cabrera 
Enviado el: martes, 4 de enero de 2022 9:24
Para: Marina Mariel Chavez <marina.chavez@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola Marina

En que formato de archivo están los padrones? Básicamente sería cruzar datos similar a un buscarv en Excel?

Yo tengo acceso a la carpeta Padrones Agentes de Recaudación, si me indicas que archivos debería cruzar y como sería más o menos el cruce puedo probar.

Supongo que esto lo necesitas hacer mensualmente.

Opciones:

1.	Probar con un complemento de Excel, con esta forma no sé si se puede automatizar. Voy a probar si funciona primero.
2.	Mi idea de hablar con los chicos de BI sería que armen algo automático que levante los archivos y te llegue por correo directamente el resultado.
3.	Con ACL sería lo mismo que el punto 2, dejarías el o los archivos que necesitas comparar y la herramienta haría todo (por ejemplo un determinado día) y el resultado con las diferencias dejar en un archivo o por correo.

Saludos.
Miguel Angel Cabrera
Auditoria interna
Tel: (54) 0362-4456000 - Interno 3820
---
De: Marina Mariel Chavez 
Enviado el: lunes, 3 de enero de 2022 15:42
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Diego lo hace con qlikview, pero no sé si tienen tantas licencias disponibles, así que yo pensé en otra herramienta.

Para colmo yo creo que me tienen que instalar el programa que vaya a utilizar. 

Vos podrías probar con ACL uno de los padrones si te indico cómo hacer el cruce? Si podes hacerlo debería solicitar a los administradores que me instalen ACL y me explicas como se trabaja.

Marina
---
De: Miguel Angel Cabrera 
Enviado el: lunes, 3 de enero de 2022 15:29
Para: Marina Mariel Chavez <marina.chavez@grupocarsa.com>
Asunto: RE: Cruce padrones-proveedores SAP

Hola Marina

Si una opción sería ACCESS o cualquier Base de Datos. La otra seria hacerlo con ACL, esto con las herramientas que tenemos y otra sería hablar con los chicos de BI que armen una consulta de ambos archivos o talas y lo puedas ver por ejemplo con Qlik.

Miguel Angel Cabrera
Auditoria interna
Tel: (54) 0362-4456000 - Interno 3820
---
De: Marina Mariel Chavez 
Enviado el: lunes, 3 de enero de 2022 15:21
Para: Miguel Angel Cabrera <miguel.cabrera@grupocarsa.com>
Asunto: Cruce padrones-proveedores SAP

Hola Miguel,

Necesito saber con qué herramienta puedo trabajar para cruzar el padrón de ARBA y de AGIP para poder controlar que los proveedores tengan el indicador correcto.

Al ser los padrones tan pesados, no puedo trabajarlos con Excel, será que se puede hacer con Access? 

Este cruce lo hacía y lo sigue haciendo Diego, le otorgan permiso y lo hace, pero ya quiero dejar de molestar a la gente y no sé con qué herramienta trabajar.

Aguardo de tu sapiencia para saber cómo puedo hacer este cruce.

Marina Mariel Chavez
Impuestos
Predio 404 - Ruta N. Avellaneda Km. 15,5 
(3500) Resistencia-Chaco
Tel: (54) 0362 – 4456 000 int.3022
marina.chavez@grupocarsa.com