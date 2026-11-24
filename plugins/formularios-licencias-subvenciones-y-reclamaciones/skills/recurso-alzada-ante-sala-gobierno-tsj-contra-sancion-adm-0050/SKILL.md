---
name: recurso-alzada-ante-sala-gobierno-tsj-contra-sancion-adm-0050
description: "Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal

> Formulario **ADM-0050** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Recurso de alzada ante la Sala de Gobierno del Tribunal Superior de Justicia contra el acuerdo desestimatorio del recurso de audiencia en justicia interpuesto frente a un acuerdo que impone una multa por supuesto fraude procesal (art. 247 LEC; art. 556 LOPJ), tramitado en pieza separada.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:recurso-alzada-ante-sala-gobierno-tsj-contra-sancion-adm-0050`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE EN LETRA (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] DENOMINACIÓN SOCIAL O NOMBRE DEL ACREEDOR (2 veces)
- [ ] Nº/AÑO (2 veces)
- [ ] COMUNIDAD AUTÓNOMA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] Nº
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 556 LOPJ
- art. 818.1 LEC
- art. 818.2 LEC
- art. 247 LEC
- art. 247.3 LEC
- art. 557 LOPJ

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

A LA SALA DE GOBIERNO DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [COMUNIDAD AUTÓNOMA]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], en el expediente gubernativo n.º [Nº/AÑO], pieza separada del juicio ordinario dimanante del monitorio n.º [Nº/AÑO], instado por [DENOMINACIÓN SOCIAL O NOMBRE DEL ACREEDOR], ante la Sala comparezco y como mejor en Derecho proceda (1), DIGO:

Se ha notificado a esta parte el acuerdo desestimatorio del recurso de audiencia en justicia interpuesto por esta representación contra el acuerdo de fecha [DÍA] de [MES] de [AÑO], que impone a nuestro/a mandante la sanción consistente en una multa de [IMPORTE EN LETRA] euros, y dentro del plazo conferido por el art. 556 LOPJ, vengo a interponer RECURSO DE ALZADA contra el citado acuerdo, con base en las siguientes

ALEGACIONES

PRIMERA

El Tribunal de Instancia sanciona a esta parte porque se opuso al requerimiento en juicio monitorio, mediante procurador y abogado, en fecha [DÍA] de [MES] de [AÑO], y cuando la acreedora [DENOMINACIÓN SOCIAL O NOMBRE DEL ACREEDOR] interpuso la demanda de juicio ordinario, no compareció la demandada, declarándosele rebelde, por lo que hubo de convocarse la audiencia previa antes de dictar sentencia de condena, por lo que se aduce un fraude procesal, multándose, a pesar de las alegaciones formuladas, en cantidad de [IMPORTE EN LETRA] euros, lo que se ha ratificado en el recurso de audiencia en justicia.

SEGUNDA

Ausencia de vicio lesivo de la buena fe procesal.

Nuestro/a mandante D./Dña. [NOMBRE Y APELLIDOS] compareció ante el requerimiento monitorio con arreglo al art. 818.1 LEC, y creemos que no pertenece a las reglas de la buena fe procesal un favorecimiento irrestricto del interés de la parte contraria, de modo que hubiera que no haberse opuesto —ya que el pago no es factible—, pero no compareció cuando se le emplazó en juicio ordinario, con arreglo al art. 818.2 LEC, que remite a las normas de arts. 404 y ss. LEC. Al adoptar esta postura, lo que hizo es forzar la prueba de la deuda, sobre la que tenía dudas, y sólo desechó la carga de personarse. Obviamente, al haberse dictado sentencia condenatoria, una posible ejecución precedente se ha retrasado, pero ello es algo que, pudiendo estar regulado de otra manera, lo está así, ya que la rebeldía en el proceso declarativo común no equivale al allanamiento, y ni siquiera a la admisión de los hechos, estando facultado el deudor a forzar el que se acuda a tal declarativo, si se opone en el monitorio.

TERCERA

Existencia de interés legítimo.

El fraude procesal supone que se burle el fin práctico de una norma reguladora del proceso, por lo que la sanción impuesta deriva de reputarse que, si el requerido en juicio monitorio se opone, el fin de la norma es que se produzca un debate con resistencia y prueba del demandado, pero de un lado, no hay nada que lo indique en el art. 818.2 LEC, puesto que hace remisión a los preceptos comunes, y nada se apunta acerca de una excepción.

En todo caso, el Tribunal bien pudo estimar que cupiera dar por terminado el proceso con sentencia, una vez declarada la rebeldía del demandado, como sanción procesal adecuada, sin tardar [PLAZO] en citar la audiencia previa, y no lo hizo, estimando luego una intencionalidad de nuestro/a mandante propia e interna, lo que supone una decisión completamente arbitraria, basada en la conjetura de un ánimo dilatorio, cuando existe un interés en defenderse como permite la ley, y por ello es interés legítimo en términos del art. 24.1 CE.

CUARTA

Ausencia de motivación y de proporcionalidad.

El art. 247 LEC establece el deber de los tribunales, en el ejercicio de la potestad sancionadora a fin de fiscalizar la buena fe procesal, el respeto de la motivación y proporcionalidad de sus sanciones.

En primer lugar, se aprecia un serio defecto de falta de motivación, contrario al art. 120.3 CE, violando los tres objetos de la misma, y que implica la nulidad del acuerdo sancionador, puesto que no excluye la arbitrariedad, no hace ningún esfuerzo de convencimiento, y tampoco permite el control de la alzada ante la Sala.

En segundo lugar, la sanción, retardado el fin del proceso por la propia lentitud del Tribunal, y condenada en firme esta parte, carece de necesidad para su fin, que sería el correcto funcionamiento de la Justicia, y podría haberse sustituido con otro mecanismo no restrictivo sancionador, según se ha mencionado.

Pero además, no guarda proporcionalidad o adecuación la multa pecuniaria, ascendente a [IMPORTE EN LETRA] euros, ya que la conducta de la parte, en el supuesto hipotético de que no tuviera interés legítimo en retardar la agresión patrimonial en vía ejecutiva, estaría sancionada suficientemente con la condena en costas, y al pago de intereses moratorios desde la reclamación en juicio monitorio del fallo de la sentencia, siendo abusiva la imposición de una multa que representa [PORCENTAJE] % del principal reclamado de [IMPORTE] euros, si se tiene en cuenta que las circunstancias del hecho de que habla el art. 247.3 LEC deben referirse al grado de culpa en el supuesto fraude procesal, que no sería nunca la generadora de todo el retraso.

Por todo lo anteriormente expuesto,

SUPLICO A LA SALA

que, por presentado este escrito, se digne admitirlo, y en mérito a lo manifestado, se acuerde revocar el acuerdo sancionador adoptado por el Tribunal de Instancia n.º [Nº] de [SEDE], y por el que se multa a nuestro/a mandante en cantidad de [IMPORTE EN LETRA] euros.

Es justicia de hacerse en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [NOMBRE Y APELLIDOS] | Firma del Procurador/a: [NOMBRE Y APELLIDOS]

NOTA (1): No deja de ser debatible que el régimen procedimental de la imposición de sanciones por vulneración de la buena fe procesal, que no se establece en el art. 247 LEC, se corresponda con las correcciones disciplinarias, y sea de aplicación el art. 557 LOPJ, y por ende, ese Título V del Libro VII de dicha Ley, pensadas como sanciones administrativas para corregir a profesionales, y no a las partes, y no por la conducta procesal, sino por desobedecer o faltar al respeto al tribunal en actuación forense, no asistir ante éste, o incumplir los deberes de representación o defensa. En todo caso, si la sanción procesal se merece en muchos casos de dilaciones abusivas, tiene poco sentido recargar al órgano sancionador con la apertura de un expediente, con alegaciones previas al acuerdo, recurso de audiencia en justicia, y una alzada.

En cualquier caso, parece que el expediente sancionador, una vez notificadas todas las partes de su apertura, se entiende solamente entre la parte sancionada y el tribunal o tribunales sancionadores.
