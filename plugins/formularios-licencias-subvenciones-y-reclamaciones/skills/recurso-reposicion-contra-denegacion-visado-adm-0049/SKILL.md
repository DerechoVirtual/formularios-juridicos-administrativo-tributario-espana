---
name: recurso-reposicion-contra-denegacion-visado-adm-0049
description: "Recurso de reposición contra la denegación del visado de reagrupación familiar de españoles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra la denegación del visado de reagrupación familiar de españoles

> Formulario **ADM-0049** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra la denegación del visado de reagrupación familiar de españoles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra la denegación del visado de reagrupación familiar de españoles” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:recurso-reposicion-contra-denegacion-visado-adm-0049`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DNI/NIE
- [ ] DÍA
- [ ] EXPONER EL MOTIVO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 112.1 Ley 39/2015
- art. 2 Real Decreto 240/2007

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

AL CONSULADO GENERAL DE ESPAÑA EN [LOCALIDAD]

D./D.ª [NOMBRE Y APELLIDOS] mayor de edad, con DNI [DNI/NIE], con domicilio a efectos de notificaciones sito en [LOCALIDAD], y con teléfono [TELÉFONO] (además, en su caso, fax y/o correo electrónico), en su propio nombre (o en representación de D. [NOMBRE Y APELLIDOS], y cuyas demás circunstancias ya constan en el procedimiento nº [Nº DE PROCEDIMIENTO]/[AÑO], que se sigue a mis instancias por solicitud de visado de reagrupación familiar, comparece y como mejor proceda, DICE:

Que en fecha [FECHA]. he sido notificado de la resolución del Consulado al que me dirijo de fecha [FECHA] por la que se denegaba el visado de residencia por reagrupación familiar solicitado por quien suscribe en relación a sus padres [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS]. y de conformidad con lo prevenido en el art. 112.1 de la Ley 39/2015, por medio del presente escrito interpongo RECURSO DE REPOSICIÓN en base a los siguientes

MOTIVOS

PRIMERO.- Infracción por inaplicación del Real Decreto 240/2007, de 16 de febrero, que regula la residencia de los ciudadanos de la Unión Europea y sus familiares, y de la interpretación del mismo realizada por la STS de 1 de junio de 2.010, contra dicho Real Decreto 240/2007, y aplicación indebida del vigente Reglamento de Extranjería aprobado por Real Decreto 557/2011, de 20 de abril.

Tal como consta en el expediente, el que suscribe ostenta la nacionalidad española por lo que le es de aplicación el régimen de reagrupación específicamente contemplado en el Real Decreto 240/2007, tal como expresa la citada STS de 1 de junio de 2010, que anuló la expresión "otro Estado miembro" contenida en el artículo 2 del Real Decreto, de manera que el Real Decreto devino aplicable también a los españoles, resultando inoperante la disposición adicional vigésima del Reglamento de Extranjería, que remitía a la regulación establecida, la cual ya no fue incorporada al Reglamento de 2011.

En consecuencia, el régimen aplicable a la reagrupación de ascendientes directos de españoles es el contemplado en el artículo 2 del Real Decreto 240/2007 que únicamente exige que el reagrupado se halle a cargo del reagrupante, tal como expresa la STS de 20 de octubre de 2.011, por lo que la resolución impugnada infringe el citado precepto al aplicar la normativa general sobre extranjería.

SEGUNDO.- Al amparo de lo dispuesto en el art. 2 del Real Decreto 240/2007, por infracción del mismo precepto, al concurrir los requisitos para la reagrupación del padre de quien suscribe, al existir dependencia económica del reagrupado.

De la documental obrante en el expediente se desprende indudablemente la situación de dependencia económica del padre del recurrente, habiéndose acreditado que periódicamente le son transferidos fondos por parte del recurrente, que tiene una avanzada edad y un estado de salud que no le permite obtener por sí mismo los medios para subvenir sus propias necesidades, puesto que está impedido para trabajar, no percibe ingresos y necesita una tercera persona que cuide del mismo. Todo ello revela la insuficiencia de los medios materiales de que disfruta en su país de origen y, en consecuencia, se acredita que es el recurrente el que está sufragando realmente sus necesidades.

Esta circunstancia justifica la concurrencia del requisito del artículo 2 del Real Decreto 240/2007, al que antes se ha hecho referencia, de hallarse el reagrupado a cargo del reagrupante, lo que es suficiente para autorizar la residencia en los términos en que fue solicitada, interesando la reposición de la resolución denegatoria por estos motivos.

TERCERO.- [EXPONER EL MOTIVO]
Por todo lo expuesto, SOLICITO tenga por presentado este escrito junto con los documentos que al mismo se acompañan, y por interpuesto recurso de reposición y, en virtud de las alegaciones contenidas en el mismo y previos los trámites legales, dicte resolución dejando sin efecto la resolución recurrida, acordando la autorización de residencia en los términos en que fue solicitada.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma

========================================================================
