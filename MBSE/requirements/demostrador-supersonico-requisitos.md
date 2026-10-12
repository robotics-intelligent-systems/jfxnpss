# Demostrador supersónico de investigación — especificación de alto nivel

**Proyecto:** jfxnpss · **Fecha:** 11 de octubre de 2026 · **Versión:** 0.1, propuesta para revisión de requisitos (SRR).

**Referencia técnica elegida por el solicitante:** Tejas/LCA Navy y TEDBF. **Modelo asociado:** [demostrador-supersonico-sysml.drawio](../CAS/Drawio/demostrador-supersonico-sysml.drawio).

## 1. Objetivo y alcance

Definir una aeronave civil experimental y su gemelo digital para investigar propulsión, resistencia aerodinámica, resistencia estructural, integración de diseño, consumo y maniobrabilidad en régimen subsónico, transónico y supersónico. La primera entrega será una configuración digital verificable; la construcción y el vuelo exigirán requisitos adicionales y una aprobación de aeronavegabilidad independiente.

La imagen `MBSE/CAD/supersonic-research-demonstrator.jpg` muestra un concepto modular con propulsión, estructuras, instrumentación y dinámica de vuelo. No contiene geometría editable, masas, mapas de motor ni resultados de ensayo. La configuración base propuesta es terrestre, monomotor, con ala delta y módulos científicos intercambiables. Una configuración bimotor se estudiará como alternativa inspirada en TEDBF. El número de motores, los canards y la geometría final siguen sujetos a evaluación; la ilustración no los congela.

Se reutilizan enseñanzas sobre integración motor–célula, control de vuelo y validación gradual. Las operaciones embarcadas, el armamento y los requisitos de combate no forman parte de la misión del demostrador. El vínculo con el proyecto marítimo se limita inicialmente al intercambio de escenarios y datos ambientales.

## 2. Localización histórica y procedencia

### Resultado de la revisión del repositorio naval

Se revisaron el árbol actual, los nombres históricos de activos CAD y los textos `.md`/`.drawio` de las **142 revisiones accesibles** del clon de jfxmbdss. No hubo coincidencias textuales para Tejas, TEDBF, F404, F414 o las expresiones indoamericano/indo-american. Esto no descarta referencias dibujadas dentro de imágenes, enlaces externos o historia no accesible.

El antecedente explícito recuperado es [SM-36-STALMA_HELLENIC_AIR_FORCE_CONCEPT.jpg](https://github.com/robotics-intelligent-systems/jfxmbdss/blob/8e7ebc09b7fd39ce0dea7eea928119153f15069b/MBSE/CAD/SM-36-STALMA_HELLENIC_AIR_FORCE_CONCEPT.jpg), añadido en [8e7ebc0](https://github.com/robotics-intelligent-systems/jfxmbdss/commit/8e7ebc09b7fd39ce0dea7eea928119153f15069b), el 25 de junio de 2026, y eliminado en [f31565f](https://github.com/robotics-intelligent-systems/jfxmbdss/commit/f31565fd6fc1f178158da2875d4a4996b83d3520), el 26 de junio. Es una referencia diferente a la confirmada por el solicitante y **no se usa para dimensionar este demostrador**.

Por tanto, Tejas/TEDBF se incorpora como referencia externa confirmada por el solicitante, sin atribuir al repositorio una ficha histórica que no se pudo localizar. La base modular offshore vigente tampoco acredita compatibilidad entre un avión concreto y su cubierta.

### Fuentes y revisiones

| ID | Fuente | Uso y límite |
|---|---|---|
| S1 | [jfxmbdss, revisión 7075e95](https://github.com/robotics-intelligent-systems/jfxmbdss/tree/7075e95c6eea70b66dbd6a39edce18229cbd1f5e) | Contexto marítimo y catálogo conceptual; no prestaciones verificadas de portaviones. |
| S2 | [jfxnpss, revisión f3c4b7d](https://github.com/robotics-intelligent-systems/jfxnpss/tree/f3c4b7dbde152e54986e5fed39eeeb6ebcb4dc78) y [activo CAD](https://github.com/robotics-intelligent-systems/jfxnpss/blob/f3c4b7dbde152e54986e5fed39eeeb6ebcb4dc78/MBSE/CAD/supersonic-research-demonstrator.jpg) | Arquitectura OpenTwin Propulsion y concepto visual. |
| S3 | [Departamento de Producción de Defensa de India: LCA Tejas](https://www.ddpmod.gov.in/en/resources/products/lca-tejas) | Ficha general de Tejas; no trasladar automáticamente sus valores a LCA Navy o TEDBF. |
| S4 | [GE: ficha F404](https://www.geaerospace.com/sites/default/files/2022-01/F404%20Family%20Data%20Sheet_UPDATED.pdf) | Valores públicos de clase de motor en condiciones de nivel del mar/día estándar. |
| S5 | [GE: F404-IN20 y prototipos navales](https://www.geaerospace.com/news/press-releases/defense-engines/f404-ge-in20-powers-tejas-aircraft-successful-first-flight) | Identificación de motor, postcombustión y control FADEC. |
| S6 | [GE: F414](https://www.geaerospace.com/military-defense/engines/f414) | F414-INS6 asociado a Tejas Mk2; referencia alternativa de clase de motor. |
| S7 | [PIB, 12 de enero de 2020: LCA Navy en INS Vikramaditya](https://www.pib.gov.in/newsite/erelcontent.aspx?lang=2&reg=48&relid=197393) | Antecedente de demostración tecnológica naval y continuidad hacia TEDBF. El calendario previsto entonces no prueba un hito posterior. |
| S8 | [PIB, 6 de febrero de 2023: aterrizaje en INS Vikrant](https://www.pib.gov.in/PressReleasePage.aspx?PRID=1896759&lang=1&reg=3) | Hito de ensayo embarcado del LCA Navy. |
| S9 | [PIB, Aero India 2025: TEDBF](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2101182&lang=1&reg=3) | Modelo a escala del futuro avión naval diseñado por ADA; no resultados de vuelo. |

Fuentes consultadas para esta versión. Las páginas web son modificables; las revisiones de los repositorios quedan fijadas arriba. Antes de congelar requisitos, archivar las fichas externas con fecha, hash y variante. Las noticias recopiladas por terceros no se consideran datos de diseño primarios.

## 3. Qué se transfiere de Tejas/TEDBF

| Aspecto | Evidencia pública | Aplicación al demostrador |
|---|---|---|
| Propulsión | Tejas usa F404-IN20; S4 declara clase de empuje 84 kN, masa de motor 1.072 kg y caudal 70 kg/s. S3 redondea el empuje con postcombustión a 85 kN. | Referencia de escala, no motor seleccionado ni empuje instalado disponible en altura. Crear un modelo genérico abierto con mapas autorizados o sintéticos identificados. |
| Alternativa de motor | S6 publica F414-INS6 para Tejas Mk2 y clase de empuje 22.000 lbf, aproximadamente 97,9 kN. | Caso comparativo de propulsión. La fuente no confirma por sí misma la selección final de motor para TEDBF; no asignar dos INS6 al diseño como hecho establecido. |
| Diseño y velocidad | S3 publica Mach 1,6 y masa máxima de despegue 13.500 kg para la ficha general del LCA. | Referencia de orden de magnitud; no fija dimensiones o masa del demostrador ni la envolvente naval. |
| Resistencia | S3 publica límites de carga +8/−3,5 g. No se obtuvo una polar de resistencia ni una base de cargas navales validada. | Adoptar un límite experimental más moderado y generar polares/cargas propias. Separar resistencia aerodinámica de resistencia estructural. |
| Control y maniobrabilidad | [PIB, Tejas IOC 2013](https://www.pib.gov.in/newsite/PrintRelease.aspx?lang=2&reg=48&relid=102056) describe control digital fly-by-wire cuádruple. | Investigar estabilidad y control con protección de envolvente; no afirmar que se dispone de sus leyes de control. |
| Investigación naval | S7–S9 separan pruebas de LCA Navy y futuro TEDBF bimotor. | Ensayos escalonados y comparación monomotor/bimotor. No heredar aterrizaje arrestado, plegado de alas o salto de cubierta. |
| Combustible | Las fuentes seleccionadas no proporcionan mapas suficientes de TSFC ni consumo por misión de LCA Navy/TEDBF. | Estimar consumo mediante ciclo y misión acoplados. No inferirlo de autonomía, capacidad de tanque o empuje máximo. |

“Indoamericano” se entiende aquí como aeronave de desarrollo indio con referencia a propulsión estadounidense; no como designación oficial o coproducción acreditada de toda la aeronave.

## 4. Hipótesis de la línea base conceptual

**P = propuesto**, **TBD = por determinar**, **TBR = por confirmar**. Todos los valores siguientes son decisiones iniciales de este estudio, no prestaciones históricas ni certificadas. Los requisitos P son verificables en el modelo, pero solo se convierten en compromisos de diseño después de la SRR.

| Parámetro | Línea base propuesta | Cierre |
|---|---|---|
| Misión | 45 min de misión nominal, con 5 min a Mach 1,2; reserva separada de 20 min subsónicos | P; especificar perfiles de ascenso, descenso y reserva antes de simular |
| Punto supersónico | Mach 1,2 a 11.000 m, atmósfera ISA, masa y carga científica declaradas | P; no exige supercrucero sin postcombustión |
| Dominio de estudio | Mach 0,2–1,6 y altitud 0–15.000 m | P; dominio de modelos, no autorización de vuelo |
| Cargas experimentales | −1 a +4 g, donde permitan presión dinámica, ángulo de ataque y límites estructurales | P; no requerir +4 g en toda la envolvente |
| Motor base | Un turbofán genérico con postcombustión opcional; F404 como referencia de clase | P; empuje seco/instalado, TSFC y transitorios TBD |
| Alternativa | Dos motores genéricos; comparar masa, consumo, control asimétrico y mantenibilidad | P; continuidad de vuelo con un motor inoperativo TBD |
| Geometría | Ala delta, fuselaje esbelto, instrumentación modular; canards opcionales | P; geometría y efecto de onda requieren estudio propio |
| Masa, ala, tanque y carga útil | MTOM, masa vacía, superficie alar, combustible utilizable y carga científica TBD | Equipo de diseño/MDAO; cierre antes de PDR |
| Resistencia y control | CD(M,Re,α,β,δ), CL, momentos, derivadas, αmax y qmax TBD | Aerodinámica/dinámica; cierre mediante modelos y evidencia |

La misión nominal y la reserva se calculan separadamente. No se autoriza iniciar un segmento si el combustible restante cae por debajo del necesario para retorno y reserva. No se fija aún una autonomía kilométrica ni un consumo en kg/h sin el dimensionamiento de misión.

## 5. Requisitos de alto nivel y aceptación

REQ-000: **El sistema deberá producir evidencia reproducible para evaluar una configuración de demostrador supersónico civil en los cinco dominios solicitados.** Se descompone en los requisitos siguientes. Prioridad M = obligatorio para la entrega digital; D = deseable. Todos tienen estado propuesto. A = análisis, T = prueba, I = inspección, Dm = demostración. El texto completo de esta tabla prevalece sobre las etiquetas abreviadas del diagrama.

| ID / prioridad | Requisito — el sistema deberá… | Criterio de aceptación y verificación | Responsable / bloque |
|---|---|---|---|
| REQ-001 / M | Representar la misión y toda condición inicial de manera explícita. | V-001, I/T: manifiesto con todos los segmentos, masas, carga útil, atmósfera, combustible y reserva; rechazo de campos obligatorios ausentes. | Integración / B-MIS |
| REQ-002 / M | Sostener en simulación el punto de investigación Mach 1,2 a 11.000 m durante 300 s. | V-002, A: Mach 1,20 ±0,02 y altura ±100 m; trimado, combustible positivo y límites térmicos/de control satisfechos durante todo el segmento, con configuración declarada. | Prestaciones / B-SYS |
| REQ-003 / M | Proporcionar empuje instalado suficiente para la misión nominal. | V-003, A: empuje disponible ≥1,05 veces el requerido en los puntos de diseño de ascenso y segmento supersónico; en crucero, mando regulable para equilibrio. Incluir pérdidas de admisión, instalación y extracción de potencia. | Propulsión / B-PROP |
| REQ-004 / M | Operar el modelo de motor dentro de sus límites de admisión, estabilidad y temperatura. | V-004, A/T: cero violaciones de los límites declarados en casos nominales; fallos y entradas fuera del dominio generan estado inválido explícito. Mapas/límites TBD impiden declarar cumplimiento. | Propulsión / B-PROP |
| REQ-005 / M | Cuantificar resistencia aerodinámica, sustentación y momentos entre Mach 0,2 y 1,6. | V-005, A: base por configuración y régimen con resistencia viscosa, inducida y de onda sin doble conteo; malla/solver documentados y al menos tres casos de referencia subsónico, transónico y supersónico. | Aerodinámica / B-AERO |
| REQ-006 / M | Mantener integridad estructural en la envolvente de cargas propuesta y bajo efectos térmicos. | V-006, A: márgenes de seguridad ≥0 a carga límite y resistencia última a 1,5 veces carga límite; considerar masa mínima/máxima, maniobra, ráfaga, aterrizaje y combinaciones térmicas. Cargas/método material TBD bloquean aprobación. | Estructuras / B-STR |
| REQ-007 / M | Evitar inestabilidad aeroelástica dentro de la envolvente experimental. | V-007, A: ninguna divergencia o flutter hasta 1,15 veces la velocidad equivalente máxima declarada, en casos de masa/combustible extremos. Modelo acoplado y margen P pendientes de revisión especializada. | Aeroelasticidad / B-STR |
| REQ-008 / M | Mantener un modelo geométrico y de masas trazable por configuración. | V-008, I/A: CAD editable con SI, ejes, versión y módulos; suma de masas consistente al 0,1%; centro de gravedad e inercias para tanque lleno, intermedio y mínimo utilizable. | Diseño / B-CAD |
| REQ-009 / M | Comparar alternativas monomotor/bimotor y ala delta con/sin canards. | V-009, A: matriz de alternativas a igual misión y carga científica; reportar masa, empuje instalado, resistencia, combustible, control, incertidumbre y compromisos; no seleccionar únicamente por apariencia. | Arquitectura / B-CAD |
| REQ-010 / M | Calcular consumo y dimensionar combustible para misión, retorno y reserva. | V-010, A: combustible utilizable ≥1,10 veces la suma nominal de misión y reserva definida; flujo integrado y cambio de masa concuerdan al 0,5%. Combustible no utilizable contabilizado aparte. | Energía / B-FUEL |
| REQ-011 / M | Separar consumo en seco y con postcombustión, y reportar incertidumbre. | V-011, A/I: TSFC, flujo, régimen y condición por segmento; sensibilidad inicial ±20% de TSFC sintético; cero mejoras porcentuales sin baseline comparable. Identificar qué datos son estimados y cuáles medidos. | Energía / B-FUEL |
| REQ-012 / M | Permitir vuelo trimado y maniobras científicas controlables dentro de límites. | V-012, A/T: trimado en puntos válidos de la matriz M/h/m/CG; a Mach 0,6 y 5.000 m ejecutar viraje coordinado de 30° durante 60 s con altura ±100 m y sin saturación sostenida >1 s; verificar cargas −1/+4 g solo donde la envolvente lo permita. | Dinámica/control / B-FCS |
| REQ-013 / M | Detectar límites y degradaciones antes de aceptar resultados de maniobra. | V-013, T: inyectar sensor inválido, actuador saturado y pérdida de empuje; marcar caso degradado, límites y recuperación/aborto. En alternativa bimotor incluir empuje asimétrico. Tiempos de respuesta y redundancia física TBD. | Control / B-FCS |
| REQ-014 / M | Medir o simular las magnitudes necesarias para verificar prestaciones. | V-014, I/T: registro sincronizado de Mach, altura, α, β, aceleraciones, tasas, combustible, empuje estimado, temperaturas y mandos; identificación de sensor, calibración, incertidumbre y origen; desfase de canales de la demostración digital ≤10 ms. | Instrumentación / B-DAQ |
| REQ-015 / M | Intercambiar datos mediante contratos explícitos entre modelos y gemelo digital. | V-015, T: contratos versionados con SI, marcos, signo, tiempo, estado y procedencia; rechazar unidades incompatibles y fallos de convergencia; replay determinista dentro de tolerancias declaradas. | Gemelo digital / B-TWIN |
| REQ-016 / M | Validar los modelos antes de declarar cumplimiento de prestaciones. | V-016, A/I: benchmarks independientes por disciplina y al menos un caso integrado; tolerancia inicial ≤10% en empuje y flujo, ≤10% en CD cuando CDref≥0,02 o error absoluto ≤0,002 para valores menores. Dominio, evidencia y errores de dinámica/estructura definidos antes de sus ensayos. | V&V / B-VV |
| REQ-017 / M | Mantener trazabilidad bidireccional de requisitos, arquitectura y evidencia. | V-017, I: 100% de requisitos con responsable, bloque «satisfy», caso «verify», configuración y resultado; cero requisitos aceptados con TBD/TBR crítico abierto. | Ingeniería de requisitos / B-VV |
| REQ-018 / D | Intercambiar escenarios con el entorno marítimo de jfxmbdss. | V-018, Dm/T: exportar/importar un escenario ambiental con unidades y reloj comunes; conservar procedencia y autoridad de cada modelo. No representa habilitación de operaciones embarcadas. | Integración / B-TWIN |

REQ-001 a REQ-018 derivan de REQ-000 y la misión civil. S3–S9 inspiran las decisiones; **no son por sí mismas evidencia de satisfacción**. Las tolerancias y márgenes son P y no equivalen a una norma de certificación.

## 6. Arquitectura funcional y contratos

| Bloque | Responsabilidad | Entradas → salidas |
|---|---|---|
| B-SYS, DemostradorInvestigacion | Integración de la aeronave y prestaciones de misión | Misión/configuración → trayectoria, viabilidad y resultados |
| B-MIS, MisionInvestigacion | Perfil de misión y condiciones de ensayo | Objetivo, ambiente, reserva → segmentos y criterios |
| B-CAD, ConfiguracionDiseno | Geometría, módulos, masa y selección de alternativas | Configuración → geometría, masa, CG, inercia |
| B-AERO, Aerodinamica | Polares y fuerzas/momentos de célula | Geometría, estado, mandos → fuerzas y momentos |
| B-STR, EstructurasTermica | Cargas, respuesta térmica y aeroelasticidad | Cargas, calor, masa → márgenes y límites |
| B-PROP, Propulsion | Admisión, ciclo, tobera y control local | M/h/atmósfera, combustible, mando → empuje, flujo, calor, límites |
| B-FUEL, CombustibleEnergia | Alimentación, balance de combustible y reserva | Demanda de flujo, misión → masa restante, reserva y CG |
| B-FCS, DinamicaControl | Dinámica 6 GDL, trimado y protección de envolvente | Fuerzas, momentos, sensores, orden → estado y actuadores |
| B-DAQ, Instrumentacion | Adquisición y calidad de datos científicos | Estado/observaciones → telemetría sincronizada |
| B-TWIN, GemeloDigital | Orquestación, contratos, historial y replay | Manifiestos/telemetría → estado versionado y resultados |
| B-VV, VerificacionValidacion | Benchmarks, aceptación y registro de evidencia | Modelos, requisitos, casos → cumplimiento y límites de validez |

La propulsión incluye admisión, compresor/fan, cámara, turbina, ejes, tobera, postcombustión opcional y control genérico. Interfaces estables permiten sustituir fidelidades. El modelo físico puede usar pyCycle/OpenMDAO, OpenModelica, OpenVSP y CFD apropiado como candidatos ya recogidos en S2; no se presume que estén integrados. El estudio 6 GDL requiere una implementación calificada para la configuración.

| Contrato | Productor → consumidor | Datos mínimos |
|---|---|---|
| IF-01, configuración | B-CAD → B-AERO/B-STR/B-PROP/B-FCS | ID/hash, m [kg], CG [m], tensor de inercia [kg·m²], S [m²], geometría, marcos |
| IF-02, estado/atmósfera | B-FCS/B-MIS → B-AERO/B-PROP | M, h [m], V [m/s], ρ [kg/m³], p [Pa], T [K], α/β [rad], tiempo [s] |
| IF-03, fuerzas | B-AERO/B-PROP → B-FCS/B-STR | Fuerzas [N], momentos [N·m], empuje instalado, signo/ejes, punto de aplicación |
| IF-04, combustible | B-PROP ↔ B-FUEL | Flujo solicitado/entregado [kg/s], masa utilizable [kg], modo, temperatura y estado de alimentación |
| IF-05, mando | B-FCS → B-PROP/actuadores | Mando normalizado y deflexión [rad], límites, latencia, validez |
| IF-06, límite térmico/estructural | B-STR/B-PROP → B-FCS/B-TWIN | Temperaturas [K], q [Pa], carga g, margen y estado de restricción |
| IF-07, telemetría/evidencia | B-DAQ ↔ B-TWIN → B-VV | runID, timestamp, configID, modelID, valor/unidad, incertidumbre, origen, calidad y fallo |

Convención inicial: ejes cuerpo x adelante, y derecha, z abajo; NED para navegación; ángulos en radianes; altitud en metros sobre nivel medio del mar. Los adaptadores transforman de forma explícita otros marcos. Distinguir magnitudes estáticas/totales, masa/peso y empuje bruto/neto/instalado. El escenario controla el reloj de simulación; la telemetría conserva además el tiempo de recepción.

## 7. Relaciones paramétricas de alto nivel

Estos balances son restricciones conceptuales, no sustituyen CFD, un ciclo de motor validado o ensayos:

```text
q = 0,5 ρ V²                         [Pa]
D = q S CD                           [N]
L = q S CL                           [N]
CD = CD_viscoso + CD_inducido + CD_onda + CD_interferencia
T_inst = Σ T_neto_motor − ΔT_instalacion
m dV/dt = T_inst − D − m g sin(γ)     (aproximación longitudinal)
dm_f/dt = −ṁ_f                       [kg/s]
m_f,misión = ∫ ṁ_f dt                 [kg]
m_f,utilizable ≥ 1,10 (m_f,misión + m_f,reserva)
TSFC = ṁ_f / T_inst                  [kg/(N·s)], solo si T_inst > 0
n = L/(m g)                          (aproximación de carga normal)
ω_viraje = g tan(φ)/V                [rad/s], viraje coordinado nivelado
MS = admisible/solicitación − 1       para criterio material definido
```

En el balance de fuerzas, separar resistencia de célula y penalizaciones de instalación para evitar contar dos veces la resistencia de admisión/tobera. En el motor y sus mapas, declarar si TSFC utiliza empuje no instalado; convertir antes de compararlo con el TSFC del sistema. Resistencia de onda/transónica y maniobras no estacionarias exigen mayor fidelidad que estos balances.

## 8. Verificación, validación y cierre

1. **SRR:** revisar misión, hipótesis, fuentes, prioridades y criterios P; asignar propietarios y aprobar la línea base de requisitos.
2. **Diseño conceptual/PDR:** cerrar masas, geometría, combustible, mapas de motor, carga útil, αmax/qmax y selección mono/bimotor. Ejecutar V-001 a V-013; conservar casos fallidos.
3. **Calificación digital:** casos independientes subsónico/transónico/supersónico; estudio de convergencia; comparar ciclo y flujo; calificar dinámica, estructura y acoplamiento. Ejecutar V-014 a V-018 y repetir los casos afectados por cambios.
4. **Ensayos físicos posteriores:** definir una especificación separada de seguridad, instrumentación y permisos; correlacionar bancos/túnel/ensayos estructurales antes de ampliar la envolvente de vuelo.

Cada V-xxx deberá registrar entradas, hash de modelos/geometría, solver y versión, referencia independiente, tolerancia predefinida, resultado, incertidumbre, fecha y revisor. Un caso que solo coincide con otro modelo sin datos independientes verifica consistencia, no valida realidad física. Los casos de V-016 pueden reutilizarse para otros requisitos, pero deben conservar su trazabilidad.

| Pendiente | Responsable | Hito de cierre / impacto |
|---|---|---|
| Mapas, TSFC seco/con postcombustión y límites de motor | Propulsión | PDR; REQ-003/004/010/011/016 |
| MTOM, masa vacía, carga científica, S, CG e inercias | Diseño | PDR; REQ-002/006/008/010/012 |
| Polares, cargas de ráfaga, material, térmica y flutter | Aero/estructuras | PDR y calificación digital; REQ-005/006/007 |
| αmax, qmax, estabilidad y leyes de control | Dinámica/control | PDR; REQ-012/013 |
| Retorno, reserva detallada y combustible no utilizable | Misión/energía | Antes del análisis de misión; REQ-001/010 |
| Configuración final y planta propulsora de TEDBF | Referencias | Antes de usar datos TEDBF cuantitativos; no bloquea el caso genérico |
| Tolerancias de validación de estructura y dinámica | V&V | Antes de ejecutar benchmarks; REQ-016 |
| Redundancia, tasas de fallos y seguridad de vuelo físico | Seguridad | Especificación posterior; no cubiertas por la aceptación digital |

**Estado de cumplimiento inicial:** no demostrado para los 18 requisitos. No se han ejecutado simulaciones ni ensayos físicos con esta entrega. El diagrama declara asignaciones previstas mediante «satisfy» y «verify», no resultados aprobados.

## 9. Uso del modelo SysML draw.io

Abrir el archivo asociado en diagrams.net. Contiene siete páginas: contexto, BDD de arquitectura, IBD de interfaces, requisitos 001–009, requisitos 010–018, restricciones paramétricas y derivación de la misión. Es una representación gráfica de **SysML 1.x de alto nivel**, editable en draw.io; no es un repositorio SysML ejecutable ni un archivo XMI.

En las páginas de requisitos, cada bloque apunta al requisito mediante «satisfy» y cada caso V-xxx apunta al mismo requisito mediante «verify». En la página de derivación, los requisitos apuntan a REQ-000 mediante «deriveReqt». B-MIS/B-TWIN/B-VV pertenecen al entorno de investigación y B-CAD es un artefacto de definición; el BDD distingue esos elementos de los subsistemas de aeronave.

Ubicación en jfxnpss: `MBSE/requirements/demostrador-supersonico-requisitos.md` y `MBSE/CAS/Drawio/demostrador-supersonico-sysml.drawio`. Los requisitos y el diagrama se entregan como una propuesta de documentación para revisión; no acreditan simulaciones ejecutadas ni prestaciones físicas.
