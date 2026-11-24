---
name: recurso-reposicion-contra-sancion-pecuniaria-adm-0014
description: "Recurso de reposición contra la sanción pecuniaria por infracción tributaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra la sanción pecuniaria por infracción tributaria

> Formulario **ADM-0014** del plugin **Reclamaciones tributarias y económico-administrativas** (`formularios-reclamaciones-tributarias`) · Administrativo y Tributario › Tributario y económico-administrativo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra la sanción pecuniaria por infracción tributaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra la sanción pecuniaria por infracción tributaria” para mi caso». También puedes invocarla directamente con `/formularios-reclamaciones-tributarias:recurso-reposicion-contra-sancion-pecuniaria-adm-0014`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamaciones-tributarias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Reclamaciones tributarias y económico-administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] EXPONER LOS HECHOS (3 veces)
- [ ] C.P. (2 veces)
- [ ] CALLE (2 veces)
- [ ] CARGO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FUNDAMENTOS (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NIF (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PISO (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EJERCICIO
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº

## Normas que cita el formulario

- art. 222 Ley 58/2003
- art. 191 LGT

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

SR. JEFE DE LA DEPENDENCIA

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio a estos efectos en (el mismo de la entidad) [LOCALIDAD], calle [CALLE], número [NÚMERO], piso [PISO], CP [C.P.], y NIF número [NIF], actuando en nombre y representación, en su condición de [CARGO] (Administrador [CARGO]) de la Entidad [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], calle [CALLE], número [NÚMERO], piso [PISO], CP [C.P.], y CIF número [NIF], ante VI comparece, y como mejor proceda en Derecho

EXPONE

Primero.— Que le ha sido notificado su acuerdo de fecha [FECHA], por el que se resuelve expediente sancionador por el Impuesto sobre Sociedades, ejercicio [EJERCICIO], con la imposición a [DENOMINACIÓN SOCIAL] (la entidad) de una sanción [ELEGIR: leve / grave / muy grave] (leve, grave o muy grave), por importe de [IMPORTE] euros ((en letra), [IMPORTE] euros (en número).

(Se acompaña copia de dicha notificación: Referencia: [Nº].)

Segundo.— Que no se ha impugnado dicho acuerdo en la vía económico–administrativa.

Tercero.— Que por tratarse de una sanción tributaria se entiende producida la suspensión automática del acto impugnado, conforme a lo dispuesto en los artículos 224.1 y 212.3 de la Ley 58/2003, de 17 de diciembre, General Tributaria.

Cuarto.— Que por estimarse dicho acuerdo improcedente, por medio del presente escrito el firmante interpone contra él recurso de reposición, y formula las siguientes Alegaciones:

HECHOS

Primero.— [EXPONER LOS HECHOS].

Segundo.— [EXPONER LOS HECHOS].

Tercero.— [EXPONER LOS HECHOS].

(Describir la operación realizada por el sujeto pasivo y los motivos argumentados por la Administración para entender que se ha producido una infracción tributaria cuyo resultado es la imposición de la sanción recurrida.)

En consecuencia, por los hechos descritos, entiende el firmante que la sanción impuesta es improcedente y debe de ser anulada, y ello en base a los siguientes.

FUNDAMENTOS DE DERECHO

Primero.— El presente recurso de reposición se interpone al amparo de lo dispuesto por los artículos 222 y siguientes de la Ley 58/2003, de 17 de diciembre, General Tributaria.

Segundo.— [FUNDAMENTOS].

Tercero.— [FUNDAMENTOS].

(Se hará referencia a las normas en las que el sujeto pasivo ampara su actuación, con referencia a la operación concreta que fue descrita en el apartado «hechos» anterior. Se observará el tipo de la infracción—artículos 191 a 206 bis LGT—, la calificación de la infracción —leve, grave o muy grave—, y si se han aplicado correctamente los criterios de graduación de las sanciones, en su caso, y se dirá, en base a normas concretas aplicables a los «hechos» anteriormente descritos, que la actuación del sujeto pasivo no es subsumible en el tipo de la infracción, o que no procede la consideración de grave o muy grave, o la aplicación de los criterios de graduación).

Por lo anteriormente expuesto entiende el firmante que la sanción impuesta objeto del presente recurso debe ser anulada.

En su virtud,

SOLICITA

Que teniendo por presentado en tiempo y forma este escrito con los documentos acompañados, se sirva admitirlo y tenga por interpuesto recurso de reposición contra el acuerdo referenciado de imposición de sanción, cuya ejecución queda suspendida automáticamente, dictando en su día resolución por la que se anule aquél por ser improcedente por los motivos expuestos.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.:

SR. INSPECTOR JEFE DE LA DEPENDENCIA DE INSPECCIÓN TRIBUTARIA DE LA DELEGACIÓN ESPECIAL DE LA AGENCIA ESTATAL DE ADMINISTRACIÓN TRIBUTARIA DE [LOCALIDAD]
