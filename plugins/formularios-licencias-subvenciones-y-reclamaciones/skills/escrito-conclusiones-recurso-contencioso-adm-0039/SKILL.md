---
name: escrito-conclusiones-recurso-contencioso-adm-0039
description: "Escrito de conclusiones en el recurso contencioso-administrativo ordinario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de conclusiones en el recurso contencioso-administrativo ordinario

> Formulario **ADM-0039** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de conclusiones en el recurso contencioso-administrativo ordinario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de conclusiones en el recurso contencioso-administrativo ordinario” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:escrito-conclusiones-recurso-contencioso-adm-0039`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] FUNDAMENTOS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 47 Ley 39/2015
- art. 48 Ley 39/2015

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

P. Ordinario /

(AL TRIBUNAL DE INSTANCIA (SECCIÓN DE LO CONTENCIOSO-ADMINISTRATIVO) N.º [NÚMERO] o A LA SALA DE LO CONTENCIOSO ADMINISTRATIVO DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [LOCALIDAD])

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo debidamente acreditado en el recurso número [Nº DE PROCEDIMIENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en aplicación del artículo 64 de la Ley reguladora de la Jurisdicción Contencioso-Administrativa formulo escrito de conclusiones con base en las siguientes

ALEGACIONES

Nos afirmamos y ratificamos en los fundamentos fácticos y legales expresados en la demanda e impugnamos los alegados de contrario en todo lo que afecten o perjudiquen nuestra posición.

Ha quedado acreditado que existen defectos formales en la tramitación del expediente de tal envergadura que deben determinar la nulidad del mismo.

Así en los folios números [Nº] se comprueba la falta de notificación personal al domicilio del denunciado, a pesar de que éste constaba claramente en los archivos de la Dirección Provincial de Tráfico, documento número [Nº DE DOCUMENTO].

Por otro lado una vez dictada la propuesta de resolución, a pesar de haberse practicado pruebas no solicitadas por mi representado, no se dio audiencia al interesado dictándose directamente más, se elevó a resolución definitiva. Así puede apreciarse en los folios [Nº], del expediente administrativo y se ha reconocido en la posición número [NÚMERO] al evacuar el trámite de confesión por la Administración.

Por estos motivos entendemos que ha de estimarse la nulidad de pleno derecho del artículo 47 de la Ley 39/2015, al vulnerarse lo establecido en el artículo 81.4 de la Ley de Tráfico.

En cuanto a los hechos en sí, también la fase probatoria ha llevado a comprobar que no ocurrieron tal como se describieron y que, por tanto, no debían considerarse como infracción.

El informe del Organismo denunciante aportado como prueba a instancia de esta parte es ambiguo e inconcreto, abandona el rigor en sus afirmaciones que había mantenido en la fase administrativa. Si a esto unimos las pruebas testificales debemos concluir que la actuación de mi representado se realizó conforme a la Ley. El testigo [NOMBRE Y APELLIDOS] es contundente en la pregunta número [NÚMERO] al responder [OTROS DATOS].

De no estimarse el motivo anterior como causa de admisión del recurso, debe apreciarse, subsidiariamente, la anulabilidad del artículo 48 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas, por incorrecta aplicación del precepto sancionador [Nº DE ARTÍCULO].

La oposición del contrario, dicho sea con los debidos respetos, se ha limitado a una mera negación de los hechos sin aportar nuevos argumentos, basando su posición exclusivamente en la fuerza probatoria privilegiada de las denuncias de la Autoridad. Sin desmerecer en ningún momento la importante labor de los Agentes de Tráfico, hay que tener en cuenta que la propia norma admite pruebas contra sus declaraciones.

Esto es lo que ha hecho esta parte, desvirtuar el contenido de la denuncia con otros medios reconocidos en derecho. El demandado no ha aportado más pruebas para confirmar su posición que ha acabado decayendo.

No se han practicado las pruebas solicitadas por esta parte consistentes en [DESCRIBIR] Interesamos que se acuerden por el Tribunal como diligencias finales.

En apoyo de nuestras pretensiones citamos, además, la siguiente jurisprudencia [FUNDAMENTOS].

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con sus copias, lo admita y tenga por evacuado el trámite de conclusiones y por instada la estimación del recurso en los términos ya expuestos en el suplico de la demanda.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
