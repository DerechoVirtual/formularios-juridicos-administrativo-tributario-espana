---
name: recurso-contencioso-administrativo-procedimiento-adm-0047
description: "Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales

> Formulario **ADM-0047** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:recurso-contencioso-administrativo-procedimiento-adm-0047`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] MES (3 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD
- [ ] PAÍS
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 8.4 LJCA

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

AL TRIBUNAL DE INSTANCIA (SECCIÓN DE LO CONTENCIOSO-ADMINISTRATIVO) DE.

D. / Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D. [NOMBRE Y APELLIDOS], según acredito mediante escritura de poder notarial que adjunto con el presente escrito, ante el Tribunal, comparezco y DIGO:

Que por medio del presente escrito interpongo, en tiempo y forma, recurso para la protección de los derechos fundamentales de la persona, contra la resolución del [ÓRGANO ADMINISTRATIVO] de fecha [FECHA] de [MES] de 20 [AÑO] por la que se denegaba la autorización de residencia en España a la interesada, copia de la cual se adjunta con el presente recurso

HECHOS

La recurrente es de nacionalidad nigeriana y está casada con D. [NOMBRE Y APELLIDOS], de nacionalidad española.

El matrimonio se encuentra inscrito en el Registro Civil de [LOCALIDAD] como se acredita mediante la certificación que se adjunta con el presente escrito.

El cónyuge de la recurrente se encuentra en la actualidad desempleado, sin una fuente estable de ingresos, motivo por el cual se dictó la resolución denegatoria que ahora se recurra.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

La competencia para conocer del recurso corresponde al Tribunal de Instancia (Sección de lo Contencioso-Administrativo) de Madrid según lo dispuesto en el art. 8.4 y 14 de la LJCA.

Legitimación

Está legitimado mi representado en virtud de lo establecido en el art. 19.1.a) de la LJC-A, por tener interés legítimo y directo en la anulación del acto objeto de impugnación.

Plazo de formulación de la demanda

Se ha respetado lo establecido en el artículo 115 LJC-A respecto al plazo de diez días para interponer el recurso.

Según estipula el art. 115 de la Ley de la Jurisdicción, a continuación se expresan los derechos cuya tutela se pretende y, los argumentos sustanciales en que se fundamenta el recurso:

a) En el presente caso se considera vulnerado el artículo 18 de la Constitución, que establece que

1.Se garantiza el derecho al honor, a la intimidad personal y familiar y a la propia imagen.

Ello porque se ha aplicado una norma (R.D 240/2007) que es transposición de una norma europea (Directiva 2004/38/CE, del Parlamento y del Consejo, de 29 de abril de 2004) que no es de aplicación al presente caso,

La Directiva 2004/38/CE establece que

1. La presente Directiva se aplicará a cualquier ciudadano de la Unión que se traslade a, o resida en [PAÍS], un Estado miembro distinto del Estado del que tenga la nacionalidad, así como a los miembros de su familia".

No este el caso del recurrente, cuyo cónyuge es española y reside en España.

La STS de 1 de junio de 2010 estableció que

el objeto de la Directiva no es regular las relaciones entre un Estado y sus nacionales, sino los derechos de libre circulación y residencia de los ciudadanos de la Unión en el espacio común y no en su país de origen. Y, de otro, se exige la necesidad de movimiento o desplazamiento, que comporta la libre circulación, para su inclusión, como beneficiario, en el ámbito de aplicación de la Directiva.

Se precisa, por tanto, que se hayan ejercitado los derechos de libre circulación y residencia para que a los miembros de su familia, que no son europeos o comunitarios, les sea de aplicación el Real Decreto 240/2007, de 16 de febrero.

Al no entenderlo así, y al denegar injustificadamente la residencia legal en España a la recurrente

b) La resolución recurrida estaría vulnerando también el artículo 14 de la Constitución Española, por cuanto se estaría discriminando a los españoles casados con cónyuges extracomunitarios respecto a aquellos casados con cónyuge español o comunitario.

La Sentencia de 28 de junio de 2013 del Tribunal de Instancia (Sección de lo Contencioso-Administrativo) Nº 3 de San Sebastian Nº 191/2013, estableció en un caso idéntico al de la recurrente que:

"(...) de suerte que se crearía una categoría de españoles ilícitamente discriminados por la circunstancia de que sus esposos/esposas no puedan residir legalmente en el Reino de España, mediante la introducción de restricciones como la que nos ocupa, de orden económicos (ingresos y seguro de enfermedad), sin perjuicio del sarcasmo que ofrece la realidad social de la crisis financiera y económica que asola el Reino de España".

Como expuso el Defensor del Pueblo en su recomendación a la Secretaría General de Inmigración y Emigración

Se ha producido pues una diferencia de trato en categorías de personas, (cónyuges de ciudadanos españoles) en situaciones subjetivas equiparables (matrimonio civil inscrito en el Registro Civil),

La distinción normativa relativa a la exigencia de medios económicos y acreditación de seguro médico a fin de disfrutar del derecho de residencia en nuestro territorio resulta una distinción infundada y discriminatoria, puesto que dicha diferencia de trato no ha sido objeto de una justificación objetiva y razonable, ni persigue una finalidad constitucionalmente legítima, ni es proporcional atendiendo a la debida ponderación de los bienes, derechos y valores en juego.

En su virtud, SUPLICO A LA SALA que, teniendo por presentado este escrito, con los documentos acompañados, se sirva admitirlo, tenerme por parte en la representación que ostento de D. Dª [NOMBRE Y APELLIDOS], y tener por interpuesto RECURSO CONTENCIOSO ADMINISTRATIVO POR LA VÍA ESPECIAL DEL PROCEDIMIENTO PARA LA PROTECCIÓN DE LOS DERECHOS FUNDAMENTALES DE LA PERSONA contra la resolución de [FECHA] de fecha [DÍA] de [MES] de [AÑO].

Por ser justicia que pido en Madrid, a [DÍA] de [MES] de [AÑO].

Fdo: Fdo:

Procurador/a Letrado/a

========================================================================
