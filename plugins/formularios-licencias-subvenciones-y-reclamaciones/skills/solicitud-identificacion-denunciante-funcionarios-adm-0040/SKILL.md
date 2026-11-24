---
name: solicitud-identificacion-denunciante-funcionarios-adm-0040
description: "Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador

> Formulario **ADM-0040** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:solicitud-identificacion-denunciante-funcionarios-adm-0040`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] C.P. (2 veces)
- [ ] CALLE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ÓRGANO ADMINISTRATIVO (2 veces)
- [ ] AÑO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NIF
- [ ] Nº DE EXPEDIENTE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 74 Real Decreto Legislativo 339/1990
- art. 87 Real Decreto Legislativo 6/2015
- art. 53.2 Ley 39/2015

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

A [ÓRGANO ADMINISTRATIVO] DE [LOCALIDAD]

D. ……………………mayor de edad, con domicilio en la C/ [CALLE] número [NÚMERO] CP [C.P.] de [LOCALIDAD] y provisto de DNI número [DNI/NIE] (o en representación de D. o de la mercantil ……………………conforme acredito con la escritura de constitución de dicha sociedad, con domicilio social en la C/ [CALLE] número [NÚMERO] CP [C.P.] de [LOCALIDAD] y CIF [NIF]), ante [ÓRGANO] de [LOCALIDAD] comparezco y, como mejor proceda en derecho, DIGO:

Que el compareciente tiene la cualidad de interesado en el Expediente sancionador que bajo el número [Nº DE EXPEDIENTE] se tramita ante esta Jefatura/Alcaldía, y al comprobar que no figuran en la denuncia los datos personales del denunciante, ni si éste es o no Agente de la Autoridad, pues tampoco aparece número de identificación alguno, por medio del presente escrito y al amparo del artículo 74 del Real Decreto Legislativo 339/1990, de 2 de marzo, que aprueba el Texto Articulado de la Ley sobre Tráfico, Circulación de Vehículos a Motor y Seguridad Vial (en adelante, Ley sobre Tráfico), en la redacción dada por la Ley 18/2009, de 23 de noviembre(art. 87 del Real Decreto Legislativo 6/2015, de 30 de Octubre, que aprueba el nuevo Texto refundido de la Ley sobre Tráfico, Circulación de Vehículos a Motor y Seguridad Vial), formulo las siguientes

Alegaciones

Que la denuncia que se nos ha notificado adolece de defecto formal al no identificarse debidamente a la persona denunciante, conforme ordena el citado artículo 74 (art. 87) de la Ley sobre Tráfico, lo cual causa indefensión, por no poder recusar, en su caso, al anónimo denunciante.

Que en dicha denuncia tampoco se identifican las personas bajo cuya responsabilidad se tramita el procedimiento, ignorando quién es su instructor y el titular del órgano competente para resolver, con lo cual se vulnera el artículo 53.2 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas.

Por ello, solicitamos se proceda a identificar al denunciante, así como al instructor del expediente y al titular del órgano competente para resolver, remitiéndose dicha información al compareciente.

En virtud de lo expuesto,

SOLICITO A [ÓRGANO ADMINISTRATIVO] DE [LOCALIDAD] tenga por presentado este escrito y por efectuadas las alegaciones que en él se contienen, se digne admitirlo y, a su tenor, se remita la información sobre la identidad del denunciante y de los funcionarios encargados de la tramitación del expediente número

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
