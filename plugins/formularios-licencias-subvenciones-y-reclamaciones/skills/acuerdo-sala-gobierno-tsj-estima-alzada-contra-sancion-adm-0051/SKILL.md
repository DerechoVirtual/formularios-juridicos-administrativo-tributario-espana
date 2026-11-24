---
name: acuerdo-sala-gobierno-tsj-estima-alzada-contra-sancion-adm-0051
description: "Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal

> Formulario **ADM-0051** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Acuerdo de la Sala de Gobierno del TSJ estimando el recurso de alzada interpuesto contra el acuerdo sancionador dictado por la Sección Civil del Tribunal de Instancia en el expediente gubernativo dejándolo sin efecto alguno.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:acuerdo-sala-gobierno-tsj-estima-alzada-contra-sancion-adm-0051`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (4 veces)
- [ ] LUGAR (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] LOCALIDAD
- [ ] Nº DE EXPEDIENTE
- [ ] NÚMERO

## Normas que cita el formulario

- art. 247.1 LEC
- art. 247.3 LEC
- art. 661.1 LEC
- art. 675.3 LEC
- art. 247 LEC
- art. 589.3 LEC
- art. 661.2 LEC
- art. 247.2 LEC

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

Notas al pie del formulario original:
(1) No deja de ser debatible que el régimen procedimental de la imposición de sanciones por vulneración de la buena fe procesal, que no se establece en el art. 247 LEC, se corresponda con las correcciones disciplinarias, y sea de aplicación el art. 557 LOPJ, y por ende, ese Título V del Libro VII de dicha Ley, pensadas, como sanciones administrativas para corregir a profesionales, y no a las partes, y no por la conducta procesal, sino por desobedecer o faltar al respeto al tribunal en actuación forense, no asistir ante éste, o incumplir los deberes de representación o defensa. En todo caso, si la sanción procesal se merece en muchos casos de dilaciones abusivas, tiene poco sentido recargar al órgano sancionador con la apertura de un expediente, con alegaciones previas al acuerdo, recurso de audiencia en justicia, y una alzada.

En cualquier caso, parece que el expediente sancionador, una vez notificadas todas las partes de su apertura, se entiende solamente entre la parte sancionada y el tribunal o tribunales sancionadores.

========================================================================


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

AUTO

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

Primero

Habiéndose conocido por la Sección Civil del Tribunal de Instancia nº [NÚMERO] de [LOCALIDAD], proceso de ejecución de sentencia condenatoria firme frente a [ACTO O RESOLUCIÓN] y celebrada subasta de inmueble propiedad de ésta, que se adjudicó la Caja de Ahorros [ENTIDAD BANCARIA], acusando infracción del deber de buena fe procesal del ocupante D./Dña. [NOMBRE Y APELLIDOS], se incoó procedimiento sancionador en expediente gubernativo nº [Nº DE EXPEDIENTE] /, que concluyó en el acuerdo de fecha [FECHA], dictado por el dicho Tribunal, con la imposición de la multa de ciento ochenta euros a dicho D./Dña. [NOMBRE Y APELLIDOS]

Segundo

El sujeto sancionado interpuso recurso de audiencia en justicia ante la Sección Civil del Tribunal de Instancia, que fue desestimado y, en consecuencia, formula el presente recurso de alzada ante esta Sala de Gobierno.

FUNDAMENTOS DE DERECHO

PRIMERO

El art. 247.1 LEC, consagra el deber de las partes litigantes de actuar con lealtad procesal, especificando en el apartado 2 de dicha norma la proscripción de abuso de derecho y el fraude de ley, como el procesal.

La buena fe procesal debe presumirse de todo litigante, por lo que se exige la motivación cumplida de la mala fe al objeto de sancionar en términos que autoriza el art. 247.3 LEC, y una vez que se motiva por el órgano del proceso en que se evidencia, la valoración de esta alzada ha de repasar si en la detección y justificación producida aparece un debido uso de las reglas de lógica y experiencia, en relación con la ley procesal.

SEGUNDO

El caso es el de un poseedor de inmueble embargado a una mercantil en ejecución de sentencia, D./Dña. [NOMBRE Y APELLIDOS], el cual fue detectado por la Caja de Ahorros ejecutante, próxima la celebración de la subasta, quien solicitó la comunicación al mismo, para que conociera de la ejecución, y presentara en plazo de diez días los títulos que justificaban su situación, conforme al art. 661.1 LEC, sin que atendiera el requerido. Puesto que pedir entonces la declaración de carencia de derecho a permanecer el ocupante supondría la suspensión de la subasta, se produjo ésta y adjudicataria la Caja de Ahorros, solicitó después el desalojo con arreglo al art. 675.3 LEC, convocándose a D./Dña. [NOMBRE Y APELLIDOS], el cual no concurrió a la comparecencia. Una vez dictado auto que ordenaba lanzarle, se le sancionó por incurso en fraude procesal.

TERCERO

En primer lugar, debe dudarse de que corresponda sancionar como parte, en términos del art. 247 LEC, a quien es tercero ocupante de una finca en el proceso de ejecución, y no ya porque se regule entre las normas del proceso de declaración, habida cuenta que la comparecencia del art. 675.3 LEC es un incidente declarativo, sino porque no tiene calidad de parte D./Dña. [NOMBRE Y APELLIDOS], y las sanciones de colaboración de terceros con el LAJ encargado de la ejecución se prevén en el art. 591, por relación a los criterios del art. 589.3 LEC.

Y en segundo lugar, el fraude de ley procesal implica el amparo de una norma de cobertura, a través de la cual se infrinja o evite la aplicación de la norma eludida o defraudada, causando un perjuicio a alguna de las partes procesales. Bien es verdad que no se requiere prueba de ninguna intencionalidad especial (Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 23 Ene. 1999, Rec. 2352/1994), sino la comprobación objetiva de que el fin efectivo de una norma procesal se burla con el apoyo en otra norma procesal que no vaya dirigida, expresa y directamente, a proteger el acto que sea, bien porque no es un supuesto extravagante, viola otros principios, o se endereza a lesionar los derechos de otros litigantes.

El art. 675.3 LEC establece un cauce incidental, rápido, concentrado y sumario, para negar o conceder en la ejecución el derecho a permanecer un ocupante en un inmueble que se venderá judicialmente o se ha vendido ya, sin que exista otro método, y sin que pueda entenderse que todo ocupante carece de derecho, puesto que al servicio de decidirlo en cada caso se dispone la norma. Y ésta define un efecto propio para la inasistencia del ocupante a la vista para la que ha sido convocado, que es la resolución de lanzamiento, sin más trámite. Por otro lado, si el ejecutante interesado, antes de la subasta, descubre al ocupante, puede pedir que se le entere de la ejecución e intime a justificar su título, pero la inconcurrencia del ocupante a dicho interés del ejecutante, carece de sanción definida en el art. 661.2 LEC, porque igualmente debe pedir la comparecencia del art. 675.3 LEC el ejecutante a fin de desalojar al ocupante.

De tal manera, ni el acto de D./Dña. [NOMBRE Y APELLIDOS], al no aportar su título primero, y no concurrir a una vista para aportarlo después, resulta nada distinto a lo que prevé la norma procesal, y en manos del ejecutante está conjurar la doble oportunidad de silencio, y aunque la Caja de Ahorros sufre la carga de instar ante el LAJ la comparecencia del art. 675.3 LEC, y se ve retardada en su posesión, es consecuencia de lo que está previsto por el legislador, y no su violación, ya que, salvo abandono de grado, nada evita la comparecencia, antes o después de la subasta.

Por ello, la medida sancionadora es evitable e inadecuada, según lo establecido en el art. 118 CE, y en el art. 247.2 LEC, y procede estimar el recurso formulado por D./Dña. [NOMBRE Y APELLIDOS]

PARTE DISPOSITIVA

Acordamos estimar el recurso de alzada interpuesto por D./Dña. [NOMBRE Y APELLIDOS] contra el acuerdo sancionador dictado por la Sección Civil del Tribunal de Instancia nºde, de fecha [FECHA], en el expediente gubernativo de referencia, y en su consecuencia, debemos dejarlo sin efecto alguno.

Devuélvanse las actuaciones al órgano de procedencia, para su conocimiento y cumplimiento, notificándose a las partes, con advertencia de que contra la presente resolución no cabe recurso alguno.

Así por este nuestro auto, lo pronunciamos, mandamos y firmamos.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Presidente/a	Firma del Magistrado/a
