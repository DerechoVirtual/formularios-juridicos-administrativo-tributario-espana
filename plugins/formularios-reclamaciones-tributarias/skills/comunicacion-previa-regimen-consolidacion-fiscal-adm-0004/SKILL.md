---
name: comunicacion-previa-regimen-consolidacion-fiscal-adm-0004
description: "Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades

> Formulario **ADM-0004** del plugin **Reclamaciones tributarias y económico-administrativas** (`formularios-reclamaciones-tributarias`) · Administrativo y Tributario › Tributario y económico-administrativo · normativa revisada el 24-11-2026.

## Qué es

Escrito de comunicación previo a la aplicación del régimen de consolidación fiscal del IS. a efectuar por la entidad dominante, y cuando ésta es un establecimiento permanente de entidad no residente en España. Se presentará antes del inicio del período impositivo aplicable al régimen. Ejercitada la opción, quedará vinculado a este régimen indefinidamente mientras no se comunique renuncia.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades” para mi caso». También puedes invocarla directamente con `/formularios-reclamaciones-tributarias:comunicacion-previa-regimen-consolidacion-fiscal-adm-0004`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamaciones-tributarias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Reclamaciones tributarias y económico-administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] DOCUMENTACIÓN APORTADA
- [ ] DOMICILIO
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] ENTIDADES DEL GRUPO FISCAL
- [ ] ENTIDADES QUE HAN OPTADO POR EL RÉGIMEN
- [ ] FECHA
- [ ] LUGAR

## Normas que cita el formulario

- art. 61.6 Ley 27/2014

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

Escrito de comunicación previo a la aplicación del régimen de consolidación fiscal del IS. a efectuar por la entidad dominante, y cuando ésta es un establecimiento permanente de entidad no residente en España. Se presentará antes del inicio del período impositivo aplicable al régimen. Ejercitada la opción, quedará vinculado a este régimen indefinidamente mientras no se comunique renuncia.


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

DELEGACIÓN CENTRAL DE GRANDES CONTRIBUYENTES [ELEGIR: DEPENDENCIA REGIONAL DE INSPECCIÓN / DELEGACIÓN] DEDE LA AGENCIA ESTATAL DE ADMINISTRACIÓN TRIBUTARIA

D./Dña. [NOMBRE Y APELLIDOS] con N.I.F. y domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], actuando como representante [ELEGIR: de la Entidad / del Establecimiento Permanente situado en España perteneciente a la entidad no residente] denominada [DENOMINACIÓN SOCIAL], con N.I.F. y domiciliada en [DOMICILIO], según acredito con el documento que acompaño:

EXPONE

1º Que a efecto de la aplicación del régimen especial de consolidación fiscal en el Impuesto sobre Sociedades, la aquí representada, como entidad representante del grupo fiscal, presenta la declaración que previene el artículo 61.6 de la Ley 27/2014, de 27 de noviembre, del Impuesto sobre Sociedades, conteniendo los datos exigidos por el artículo 47 de su Reglamento aprobado por Real Decreto 634/2015, de 10 de julio; lo que hace con anterioridad al período impositivo en que es de aplicación este régimen especial.

2º Que a tales efectos manifiesta lo siguiente:

[OPCIONAL — incluir si procede]

(En el caso de establecimiento permanente de entidades no residentes que tengan la condición de dominantes)

- Siendo entidad dominante del Grupo un establecimiento permanente de una Entidad no residente en territorio español se manifiesta que la entidad no residente en territorio español a la que pertenece aquella es [DENOMINACIÓN SOCIAL], cuyos datos de identificación son [OTROS DATOS].

- Las entidades que integran el grupo fiscal, así como sus datos identificativos y su N.I.F. son: [ENTIDADES DEL GRUPO FISCAL].
- La aplicación del régimen de consolidación fiscal se ha acordado por todas y cada una de las entidades que integran el grupo fiscal, y sus acuerdos han sido adoptados por el Consejo de Administración, en el período impositivo inmediato anterior al que es de aplicación el régimen de consolidación fiscal, y no han sido impugnados ni son susceptibles de impugnación. Se acompaña copia de los acuerdos por los que las entidades del grupo han optado por el régimen de consolidación fiscal, cuyos datos identificativos son éstos: [ENTIDADES QUE HAN OPTADO POR EL RÉGIMEN].
- El porcentaje de participación directo o indirecto mantenido por la entidad dominante respecto de todas y cada una de las entidades que integran el grupo fiscal, así como la fecha de adquisición de las respectivas participaciones son: [OTROS DATOS].

3º Que la compareciente, como Establecimiento Permanente situado en España perteneciente a una Entidad no residente manifiesta que se cumplen todos los requisitos establecidos en el artículo 58 de la Ley del Impuesto sobre Sociedades. Y que solicita se comunique el número que se ha otorgado al grupo fiscal.

4º Que con este escrito aporta la siguiente documentación: [DOCUMENTACIÓN APORTADA].

Por todo ello,

SOLICITO

Tenga por presentado este escrito con los documentos acompañados, por comunicados los acuerdos adoptados por la junta de accionistas (u órgano equivalente) de todas las entidades que componen el grupo fiscal, con anterioridad al inicio del período impositivo en que es de aplicación el régimen de consolidación fiscal, y notifique cual es el número que se otorga al grupo fiscal.

En [LUGAR], a [FECHA].

Fdo.:

D./Dña. [NOMBRE Y APELLIDOS]
