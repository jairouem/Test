{
  "metadata": {
    "module_id": "05_QUAL_10",
    "module_code": "QUAL",
    "module_name": "Quality Assurance",
    "file_name": "05_QUAL_10_Quality_Assurance.md",
    "module_type": "quality_assurance",
    "framework_name": "Zadex AI Framework",
    "product_name": "{{PRODUCT_NAME}}",
    "product_version": "{{PRODUCT_VERSION}}",
    "owner": "Jairo García",
    "status": "active",
    "language": "es-ES",
    "description": "Módulo transversal encargado de validar, puntuar, corregir y autorizar los resultados generados antes de su entrega al usuario."
  },
  "module_scope": {
    "purpose": "Garantizar que cada resultado sea correcto, útil, coherente, seguro, trazable y conforme con la solicitud del usuario y con la configuración activa del producto.",
    "responsibilities": [
      "Validar el cumplimiento de la solicitud del usuario.",
      "Comprobar la coherencia interna del resultado.",
      "Detectar errores, contradicciones, omisiones y contenido inventado.",
      "Evaluar la calidad mediante criterios objetivos.",
      "Aplicar correcciones automáticas cuando sean seguras.",
      "Bloquear entregas que no alcancen los requisitos mínimos.",
      "Registrar internamente las validaciones y correcciones realizadas.",
      "Entregar únicamente versiones finales aprobadas."
    ],
    "excluded_responsibilities": [
      "Definir la configuración funcional del producto.",
      "Dirigir el flujo conversacional.",
      "Generar conocimiento experto.",
      "Seleccionar el modelo de inteligencia artificial.",
      "Definir la identidad visual o verbal de Zadex.",
      "Determinar obligaciones legales.",
      "Modificar el objetivo original del usuario."
    ]
  },
  "dependencies": {
    "required_modules": [
      "01_CORE_10_Framework.md",
      "02_BUSI_10_Product_Configuration.md",
      "03_CONV_10_Conversation_Orchestrator.md",
      "04_KNOW_10_Knowledge_Engine.md"
    ],
    "optional_modules": [
      "06_BRND_10_Zadex_DNA.md",
      "07_MODL_10_Model_Orchestrator.md",
      "07_MODL_20_Zadex_Framework.md",
      "08_LEGL_10_Legal_and_Governance.md"
    ],
    "execution_position": "after_generation_before_delivery",
    "dependency_rules": [
      "La validación debe utilizar la configuración efectiva del producto.",
      "La intención y las restricciones del usuario prevalecen sobre las preferencias internas de estilo.",
      "Las evidencias proporcionadas por el Knowledge Engine deben conservar su trazabilidad.",
      "Las restricciones legales o de seguridad no pueden ser anuladas por una corrección automática.",
      "La ausencia de un módulo opcional no debe impedir las comprobaciones generales de calidad."
    ]
  },
  "quality_engine": {
    "enabled": true,
    "automatic": true,
    "validate_before_delivery": true,
    "validate_after_material_change": true,
    "never_show_unapproved_versions": true,
    "maximum_validation_cycles": 3,
    "stop_when_approved": true,
    "stop_when_unrepairable": true,
    "default_delivery_threshold": 8.5,
    "critical_failure_blocks_delivery": true,
    "workflow": [
      "Recibir el resultado candidato y su contexto de generación.",
      "Reconstruir los requisitos verificables de la solicitud.",
      "Ejecutar las validaciones obligatorias.",
      "Clasificar las incidencias detectadas.",
      "Calcular la puntuación de calidad.",
      "Aplicar correcciones automáticas permitidas.",
      "Revalidar el resultado corregido.",
      "Aprobar, degradar, regenerar o bloquear la entrega.",
      "Conservar un informe interno de la decisión."
    ]
  },
  "quality_context": {
    "required_inputs": [
      "Solicitud original del usuario.",
      "Últimas instrucciones vigentes.",
      "Restricciones explícitas de formato.",
      "Idioma solicitado.",
      "Resultado candidato.",
      "Fuentes y evidencias utilizadas.",
      "Configuración activa del producto.",
      "Estado de la conversación.",
      "Advertencias emitidas por otros módulos."
    ],
    "optional_inputs": [
      "Perfil del usuario.",
      "Historial conversacional relevante.",
      "Rúbrica específica del producto.",
      "Plantilla de salida.",
      "Ejemplos aprobados.",
      "Restricciones de marca.",
      "Restricciones legales."
    ],
    "context_rules": [
      "No validar una respuesta de forma aislada cuando dependa de instrucciones anteriores.",
      "Resolver referencias ambiguas utilizando únicamente el contexto disponible.",
      "No inventar requisitos ausentes.",
      "Distinguir entre requisitos obligatorios, preferencias y sugerencias.",
      "Utilizar siempre la versión más reciente de una instrucción corregida por el usuario."
    ]
  },
  "requirement_extraction": {
    "enabled": true,
    "requirement_types": [
      "objective",
      "content",
      "format",
      "language",
      "tone",
      "length",
      "audience",
      "accuracy",
      "source",
      "temporal",
      "privacy",
      "security",
      "legal",
      "delivery"
    ],
    "requirement_schema": {
      "requirement_id": "Identificador interno único.",
      "type": "Tipo de requisito.",
      "description": "Condición verificable.",
      "priority": "critical | mandatory | preferred | optional",
      "source": "user | product | framework | legal | inferred",
      "validation_method": "Método utilizado para comprobar el requisito.",
      "status": "met | partially_met | unmet | not_applicable"
    },
    "rules": [
      "Los requisitos explícitos del usuario deben marcarse como obligatorios salvo indicación contraria.",
      "Las inferencias nunca deben tratarse como requisitos críticos.",
      "Un requisito contradictorio debe escalarse al Conversation Orchestrator.",
      "La evaluación debe basarse en requisitos observables y no en preferencias subjetivas del evaluador."
    ]
  },
  "quality_dimensions": {
    "objective_alignment": {
      "weight": 18,
      "description": "Grado en que el resultado responde exactamente a la solicitud.",
      "critical": true
    },
    "accuracy": {
      "weight": 17,
      "description": "Precisión factual, lógica, técnica y numérica.",
      "critical": true
    },
    "completeness": {
      "weight": 12,
      "description": "Cobertura suficiente de los requisitos relevantes.",
      "critical": false
    },
    "consistency": {
      "weight": 10,
      "description": "Ausencia de contradicciones internas y externas.",
      "critical": false
    },
    "grounding": {
      "weight": 10,
      "description": "Correspondencia entre afirmaciones, evidencias y fuentes.",
      "critical": true
    },
    "clarity": {
      "weight": 9,
      "description": "Facilidad de comprensión y precisión del lenguaje.",
      "critical": false
    },
    "structure": {
      "weight": 7,
      "description": "Organización lógica y adecuación del formato.",
      "critical": false
    },
    "user_value": {
      "weight": 7,
      "description": "Utilidad práctica del resultado para el usuario.",
      "critical": false
    },
    "professionalism": {
      "weight": 5,
      "description": "Nivel profesional y adecuación al contexto.",
      "critical": false
    },
    "safety_and_compliance": {
      "weight": 5,
      "description": "Cumplimiento de restricciones de seguridad, privacidad y legalidad.",
      "critical": true
    },
    "weight_validation": {
      "expected_total": 100,
      "fail_if_total_differs": true
    }
  },
  "validation_layers": {
    "layer_1_structure": {
      "purpose": "Comprobar que el resultado tiene una estructura válida y utilizable.",
      "checks": [
        "Formato solicitado.",
        "Sintaxis válida.",
        "Campos obligatorios.",
        "Ausencia de secciones rotas.",
        "Cierre correcto de bloques.",
        "Consistencia de nombres y claves."
      ]
    },
    "layer_2_instruction_compliance": {
      "purpose": "Comprobar el cumplimiento de las instrucciones del usuario y del producto.",
      "checks": [
        "Objetivo principal.",
        "Restricciones explícitas.",
        "Idioma.",
        "Extensión.",
        "Formato.",
        "Audiencia.",
        "Nivel de detalle.",
        "Elementos prohibidos."
      ]
    },
    "layer_3_content_quality": {
      "purpose": "Evaluar la calidad sustantiva del contenido.",
      "checks": [
        "Claridad.",
        "Coherencia.",
        "Completitud.",
        "Relevancia.",
        "Precisión terminológica.",
        "Ausencia de repeticiones.",
        "Utilidad práctica."
      ]
    },
    "layer_4_factual_integrity": {
      "purpose": "Validar hechos, cálculos, fuentes, referencias y afirmaciones.",
      "checks": [
        "Afirmaciones respaldadas.",
        "Fuentes correctamente atribuidas.",
        "Datos temporales actualizados.",
        "Cálculos correctos.",
        "Ausencia de citas inventadas.",
        "Separación entre hechos, inferencias y opiniones."
      ]
    },
    "layer_5_risk_and_compliance": {
      "purpose": "Detectar riesgos de seguridad, privacidad, legalidad o reputación.",
      "checks": [
        "Datos personales innecesarios.",
        "Información confidencial.",
        "Contenido restringido.",
        "Recomendaciones de alto riesgo.",
        "Afirmaciones legales no cualificadas.",
        "Instrucciones potencialmente perjudiciales."
      ]
    },
    "layer_6_delivery_readiness": {
      "purpose": "Confirmar que la versión puede entregarse directamente.",
      "checks": [
        "No contiene notas internas.",
        "No contiene marcadores sin resolver.",
        "No incluye razonamiento privado.",
        "No muestra versiones intermedias.",
        "No menciona procesos internos innecesarios.",
        "Incluye enlaces o archivos prometidos cuando corresponda."
      ]
    }
  },
  "universal_checks": [
    {
      "check_id": "QA-GEN-001",
      "question": "¿Responde exactamente a la petición vigente del usuario?",
      "severity_if_failed": "critical"
    },
    {
      "check_id": "QA-GEN-002",
      "question": "¿Se han respetado todas las restricciones explícitas?",
      "severity_if_failed": "critical"
    },
    {
      "check_id": "QA-GEN-003",
      "question": "¿Falta información necesaria para cumplir el objetivo?",
      "severity_if_failed": "major"
    },
    {
      "check_id": "QA-GEN-004",
      "question": "¿Existe información irrelevante o no solicitada?",
      "severity_if_failed": "minor"
    },
    {
      "check_id": "QA-GEN-005",
      "question": "¿Hay contradicciones internas?",
      "severity_if_failed": "major"
    },
    {
      "check_id": "QA-GEN-006",
      "question": "¿Se diferencia con claridad entre hechos, estimaciones e inferencias?",
      "severity_if_failed": "major"
    },
    {
      "check_id": "QA-GEN-007",
      "question": "¿El lenguaje es comprensible para la audiencia?",
      "severity_if_failed": "minor"
    },
    {
      "check_id": "QA-GEN-008",
      "question": "¿El formato puede utilizarse directamente?",
      "severity_if_failed": "major"
    },
    {
      "check_id": "QA-GEN-009",
      "question": "¿Existen errores ortográficos, gramaticales o tipográficos?",
      "severity_if_failed": "minor"
    },
    {
      "check_id": "QA-GEN-010",
      "question": "¿Se han eliminado repeticiones y redundancias?",
      "severity_if_failed": "minor"
    },
    {
      "check_id": "QA-GEN-011",
      "question": "¿Se mantiene el idioma solicitado?",
      "severity_if_failed": "major"
    },
    {
      "check_id": "QA-GEN-012",
      "question": "¿La respuesta contiene marcadores, variables o textos provisionales sin resolver?",
      "severity_if_failed": "critical"
    }
  ],
  "content_type_checks": {
    "analysis": [
      "Las conclusiones derivan de los datos disponibles.",
      "Las hipótesis están identificadas como tales.",
      "No se confunde correlación con causalidad.",
      "Las limitaciones relevantes están declaradas.",
      "Las recomendaciones se relacionan con los hallazgos."
    ],
    "recommendation": [
      "La recomendación responde a los criterios del usuario.",
      "Se consideran restricciones de coste, tiempo y riesgo.",
      "No se presenta una preferencia subjetiva como conclusión objetiva.",
      "Las alternativas relevantes no se omiten sin justificación.",
      "La recomendación final es accionable."
    ],
    "summary": [
      "Conserva las ideas esenciales.",
      "No introduce información que no estaba en la fuente.",
      "No altera el sentido original.",
      "Respeta la extensión solicitada.",
      "Distingue claramente los puntos principales."
    ],
    "creative_content": [
      "Cumple el briefing.",
      "Mantiene consistencia de tono y estilo.",
      "Evita repeticiones involuntarias.",
      "No reproduce de forma indebida contenido protegido.",
      "El contenido es original y adecuado a la audiencia."
    ],
    "code": [
      "La sintaxis es válida para el lenguaje indicado.",
      "Las dependencias están identificadas.",
      "El código gestiona errores previsibles.",
      "Los nombres son comprensibles.",
      "No contiene secretos ni credenciales.",
      "El ejemplo puede ejecutarse con cambios mínimos.",
      "Los comentarios aportan valor y no duplican el código."
    ],
    "json": [
      "El JSON es sintácticamente válido.",
      "No existen claves duplicadas dentro del mismo objeto.",
      "Las comillas, llaves y corchetes están correctamente cerrados.",
      "Los tipos de datos son coherentes.",
      "No hay comentarios incompatibles con JSON.",
      "Las referencias entre módulos utilizan nombres vigentes.",
      "Las variables de plantilla están declaradas o son reconocibles."
    ],
    "table": [
      "Las columnas responden al objetivo.",
      "Las unidades están indicadas.",
      "Los valores comparables utilizan el mismo criterio.",
      "Los totales y porcentajes son correctos.",
      "No existen filas o columnas ambiguas.",
      "La tabla sigue siendo legible."
    ],
    "email": [
      "El destinatario y el propósito son claros.",
      "El asunto es coherente con el cuerpo.",
      "El tono es adecuado a la relación.",
      "Las fechas, importes y compromisos son correctos.",
      "La llamada a la acción es inequívoca.",
      "No se incluyen datos sensibles innecesarios."
    ],
    "document": [
      "La jerarquía de títulos es coherente.",
      "No hay secciones duplicadas.",
      "Las referencias internas funcionan.",
      "El contenido mantiene uniformidad terminológica.",
      "La estructura permite localizar rápidamente la información."
    ],
    "presentation": [
      "Cada diapositiva tiene un propósito claro.",
      "La densidad de información es adecuada.",
      "Los títulos comunican la conclusión principal.",
      "Las cifras y gráficos son legibles.",
      "Existe continuidad narrativa.",
      "El contenido cabe dentro del formato previsto."
    ]
  },
  "factual_validation": {
    "enabled": true,
    "claim_classification": [
      "verified_fact",
      "supported_fact",
      "inference",
      "estimate",
      "opinion",
      "unknown"
    ],
    "rules": [
      "Una afirmación específica debe estar respaldada cuando existan fuentes disponibles.",
      "No inventar autores, enlaces, citas, estadísticas, fechas o referencias.",
      "No atribuir a una fuente una afirmación que la fuente no respalda.",
      "No presentar una estimación como dato confirmado.",
      "Las cifras deben conservar sus unidades, escala, moneda y periodo.",
      "Los hechos potencialmente cambiantes deben validarse con información vigente.",
      "Cuando no pueda verificarse una afirmación relevante, debe expresarse la incertidumbre."
    ],
    "citation_checks": [
      "La cita existe.",
      "La cita apunta a la fuente correcta.",
      "La fuente respalda la afirmación asociada.",
      "La atribución no exagera el contenido original.",
      "La cita se sitúa junto a la afirmación correspondiente."
    ],
    "hallucination_indicators": [
      "Detalles excesivamente específicos sin evidencia.",
      "Nombres, fechas o cifras no presentes en las fuentes.",
      "Referencias bibliográficas incompletas o improbables.",
      "Capacidades técnicas atribuidas sin confirmación.",
      "Conclusiones categóricas basadas en información parcial.",
      "Citas textuales no verificables."
    ],
    "failure_action": "repair_or_block"
  },
  "numerical_validation": {
    "enabled": true,
    "checks": [
      "Operaciones aritméticas.",
      "Porcentajes.",
      "Totales.",
      "Promedios.",
      "Conversiones.",
      "Unidades.",
      "Escalas numéricas.",
      "Redondeos.",
      "Coherencia entre cifras escritas y cifras tabuladas."
    ],
    "rules": [
      "Recalcular las operaciones relevantes antes de entregar.",
      "No mezclar monedas sin indicar el tipo de cambio.",
      "No mezclar periodos temporales no comparables.",
      "Indicar cuándo una cifra es aproximada.",
      "Los porcentajes de una distribución completa deben sumar 100 salvo justificación.",
      "El redondeo no debe alterar de forma material la conclusión."
    ],
    "tolerance": {
      "default_absolute": 0.01,
      "default_percentage_points": 0.1,
      "allow_context_override": true
    }
  },
  "temporal_validation": {
    "enabled": true,
    "checks": [
      "Vigencia de los datos.",
      "Coherencia entre fechas.",
      "Uso correcto de ayer, hoy y mañana.",
      "Identificación del periodo de referencia.",
      "Caducidad de precios, leyes, cargos, versiones y disponibilidad."
    ],
    "rules": [
      "Convertir referencias relativas en fechas concretas cuando exista riesgo de ambigüedad.",
      "No utilizar como actual un dato cuyo periodo no pueda determinarse.",
      "Distinguir entre fecha de publicación, fecha de actualización y periodo del dato.",
      "Marcar como histórica la información que ya no sea vigente.",
      "No asumir que una versión anterior sigue activa."
    ]
  },
  "consistency_validation": {
    "enabled": true,
    "consistency_domains": [
      "Terminología.",
      "Nombres propios.",
      "Fechas.",
      "Importes.",
      "Unidades.",
      "Versiones.",
      "Estados.",
      "Numeración.",
      "Referencias de archivos.",
      "Decisiones previamente aceptadas."
    ],
    "rules": [
      "Un mismo concepto debe utilizar una denominación estable.",
      "Una corrección posterior del usuario sustituye al dato anterior.",
      "No mantener simultáneamente dos valores incompatibles.",
      "Las dependencias entre módulos deben usar nombres de archivo vigentes.",
      "Los estados del workflow deben corresponder con los definidos por el orquestador."
    ]
  },
  "format_validation": {
    "enabled": true,
    "supported_formats": [
      "plain_text",
      "markdown",
      "json",
      "yaml",
      "html",
      "csv",
      "table",
      "code",
      "document",
      "spreadsheet",
      "presentation",
      "image",
      "email"
    ],
    "rules": [
      "Respetar el formato solicitado por el usuario.",
      "No sustituir un formato solicitado por otro sin justificación.",
      "No añadir títulos o explicaciones cuando el usuario solicite únicamente el contenido.",
      "No envolver JSON puro con texto dentro del mismo bloque.",
      "No utilizar tablas cuando reduzcan la legibilidad.",
      "Los archivos generados deben abrirse y conservar su estructura.",
      "Los enlaces de descarga deben corresponder a archivos realmente creados."
    ]
  },
  "language_validation": {
    "enabled": true,
    "default_language": "es-ES",
    "checks": [
      "Idioma principal.",
      "Cambio involuntario de idioma.",
      "Ortografía.",
      "Gramática.",
      "Puntuación.",
      "Terminología profesional.",
      "Registro adecuado.",
      "Consistencia regional."
    ],
    "rules": [
      "Mantener el idioma utilizado o solicitado por el usuario.",
      "No traducir nombres propios, marcas o términos técnicos consolidados sin necesidad.",
      "Evitar mezclar variantes regionales de forma inconsistente.",
      "No corregir deliberadamente expresiones que formen parte de una cita.",
      "El estilo nunca debe alterar el significado."
    ]
  },
  "privacy_and_security_validation": {
    "enabled": true,
    "checks": [
      "Datos personales.",
      "Credenciales.",
      "Tokens.",
      "Claves privadas.",
      "Información bancaria.",
      "Información médica.",
      "Información contractual confidencial.",
      "Datos internos de clientes.",
      "Metadatos técnicos sensibles."
    ],
    "rules": [
      "No exponer secretos o credenciales en la salida.",
      "Minimizar los datos personales incluidos.",
      "No reutilizar información privada fuera del contexto autorizado.",
      "Ocultar valores sensibles cuando no sean necesarios.",
      "No afirmar que un dato es público sin evidencia.",
      "Escalar al módulo legal cuando exista una duda material de cumplimiento."
    ]
  },
  "issue_management": {
    "severity_levels": {
      "critical": {
        "description": "Impide la entrega.",
        "examples": [
          "Incumplimiento del objetivo principal.",
          "Contenido inventado material.",
          "Riesgo grave de seguridad o privacidad.",
          "Formato inutilizable.",
          "Contradicción que cambia la conclusión.",
          "Archivo corrupto."
        ],
        "delivery_allowed": false
      },
      "major": {
        "description": "Reduce de forma significativa la utilidad o fiabilidad.",
        "examples": [
          "Omisión relevante.",
          "Cálculo incorrecto.",
          "Fuente insuficiente.",
          "Incumplimiento parcial de formato.",
          "Ambigüedad material."
        ],
        "delivery_allowed": false
      },
      "minor": {
        "description": "No impide el uso, pero debe corregirse cuando sea posible.",
        "examples": [
          "Repetición.",
          "Redacción mejorable.",
          "Inconsistencia menor.",
          "Problema leve de formato."
        ],
        "delivery_allowed": true
      },
      "observation": {
        "description": "Oportunidad de mejora no obligatoria.",
        "examples": [
          "Alternativa estilística.",
          "Posible ampliación.",
          "Preferencia no especificada."
        ],
        "delivery_allowed": true
      }
    },
    "issue_schema": {
      "issue_id": "Identificador único.",
      "severity": "critical | major | minor | observation",
      "category": "Categoría de la incidencia.",
      "description": "Descripción verificable.",
      "location": "Ubicación dentro del resultado.",
      "evidence": "Prueba que sustenta la incidencia.",
      "repairability": "automatic | regeneration | clarification | manual | not_repairable",
      "recommended_action": "Acción propuesta.",
      "status": "open | repaired | accepted | escalated"
    }
  },
  "scoring_engine": {
    "enabled": true,
    "scale_minimum": 0,
    "scale_maximum": 10,
    "calculation_method": "weighted_average",
    "rounding_decimals": 1,
    "score_labels": {
      "9.5-10.0": "Excelente",
      "9.0-9.4": "Muy alto",
      "8.5-8.9": "Aprobado para entrega",
      "7.0-8.4": "Requiere mejora",
      "5.0-6.9": "Insuficiente",
      "0.0-4.9": "Rechazado"
    },
    "delivery_threshold": 8.5,
    "automatic_repair_threshold": 7.0,
    "regeneration_threshold": 5.0,
    "critical_override": true,
    "major_issue_override": true,
    "rules": [
      "Una incidencia crítica abierta bloquea la entrega con independencia de la puntuación.",
      "Una incidencia mayor abierta bloquea la entrega salvo degradación explícitamente aceptada.",
      "La puntuación no debe utilizarse para ocultar incumplimientos obligatorios.",
      "Las dimensiones no aplicables deben excluirse y los pesos restantes deben normalizarse.",
      "La evaluación debe conservar una justificación interna por dimensión."
    ]
  },
  "automatic_repair": {
    "enabled": true,
    "maximum_cycles": 3,
    "allowed_repairs": [
      "Corregir errores ortográficos y gramaticales.",
      "Eliminar repeticiones.",
      "Simplificar frases confusas.",
      "Reordenar contenido para mejorar la estructura.",
      "Corregir formato y sintaxis.",
      "Resolver inconsistencias terminológicas.",
      "Recalcular operaciones verificables.",
      "Eliminar contenido irrelevante.",
      "Añadir advertencias de incertidumbre.",
      "Ajustar la extensión al requisito.",
      "Completar campos obligatorios utilizando información disponible."
    ],
    "restricted_repairs": [
      "Introducir hechos no presentes en las fuentes.",
      "Modificar cifras sin evidencia.",
      "Cambiar el objetivo del usuario.",
      "Eliminar una restricción obligatoria.",
      "Cambiar una conclusión material sin regenerar el razonamiento.",
      "Inventar citas o referencias.",
      "Suponer preferencias no declaradas.",
      "Modificar contenido legal sensible sin validación."
    ],
    "repair_strategy": [
      "Aplicar primero correcciones deterministas.",
      "Aplicar después correcciones de claridad y estructura.",
      "Revalidar todas las dimensiones afectadas.",
      "Regenerar únicamente la sección afectada cuando sea posible.",
      "Regenerar el resultado completo cuando exista contaminación estructural.",
      "Solicitar aclaración únicamente cuando no sea posible resolver una ambigüedad material."
    ],
    "meaning_preservation": true
  },
  "regeneration_policy": {
    "enabled": true,
    "triggers": [
      "Puntuación inferior al umbral de regeneración.",
      "Dos o más incidencias mayores relacionadas.",
      "Una alucinación material.",
      "Incumplimiento estructural generalizado.",
      "Pérdida del objetivo principal.",
      "Correcciones parciales que generan nuevas contradicciones."
    ],
    "modes": [
      "section_regeneration",
      "full_regeneration",
      "model_reselection",
      "knowledge_retrieval_retry",
      "conversation_clarification"
    ],
    "rules": [
      "No repetir exactamente la misma estrategia que produjo el fallo.",
      "Conservar los requisitos originales durante la regeneración.",
      "No degradar una restricción para alcanzar el umbral.",
      "Registrar internamente la causa de regeneración.",
      "Finalizar cuando se alcance el máximo de ciclos."
    ]
  },
  "delivery_decision": {
    "possible_statuses": [
      "approved",
      "approved_with_internal_observations",
      "repair_required",
      "regeneration_required",
      "clarification_required",
      "blocked"
    ],
    "decision_rules": {
      "approved": [
        "Puntuación igual o superior al umbral.",
        "Sin incidencias críticas abiertas.",
        "Sin incidencias mayores abiertas.",
        "Todos los requisitos obligatorios cumplidos."
      ],
      "approved_with_internal_observations": [
        "Puntuación igual o superior al umbral.",
        "Únicamente observaciones o incidencias menores no materiales.",
        "Resultado utilizable sin riesgo."
      ],
      "repair_required": [
        "Existen incidencias reparables.",
        "La puntuación se encuentra dentro del rango de mejora.",
        "No se ha superado el máximo de ciclos."
      ],
      "regeneration_required": [
        "La reparación local no garantiza la coherencia.",
        "Existe un fallo material de contenido.",
        "La puntuación es inferior al umbral de regeneración."
      ],
      "clarification_required": [
        "Existen requisitos obligatorios incompatibles.",
        "Falta un dato imprescindible que solo puede aportar el usuario.",
        "La ambigüedad puede cambiar materialmente el resultado."
      ],
      "blocked": [
        "Se ha alcanzado el máximo de ciclos sin aprobación.",
        "Existe un riesgo no mitigable.",
        "La solicitud no puede cumplirse de forma fiable.",
        "El resultado sigue conteniendo incidencias críticas."
      ]
    }
  },
  "fallback_behavior": {
    "when_quality_cannot_be_guaranteed": [
      "No presentar el contenido como definitivo.",
      "Reducir el alcance a afirmaciones verificables.",
      "Explicar únicamente la limitación necesaria para el usuario.",
      "Solicitar el dato mínimo imprescindible.",
      "No rellenar huecos mediante invención.",
      "No mostrar puntuaciones internas salvo solicitud expresa."
    ],
    "when_source_is_incomplete": [
      "Indicar que la conclusión es parcial.",
      "Separar lo confirmado de lo no confirmado.",
      "Evitar afirmaciones categóricas.",
      "No extrapolar más allá de la evidencia."
    ],
    "when_format_cannot_be_generated": [
      "Informar de la limitación real.",
      "Ofrecer el formato alternativo más cercano únicamente cuando resulte útil.",
      "No afirmar que se ha creado un archivo inexistente."
    ]
  },
  "quality_report": {
    "generate_internal_report": true,
    "show_to_user_by_default": false,
    "show_when_requested": true,
    "internal_report_schema": {
      "validation_id": "Identificador de la validación.",
      "timestamp": "Fecha y hora de validación.",
      "product_version": "Versión activa del producto.",
      "result_type": "Tipo de resultado evaluado.",
      "requirements": "Requisitos verificados.",
      "dimension_scores": "Puntuaciones por dimensión.",
      "issues": "Incidencias detectadas.",
      "repairs": "Correcciones aplicadas.",
      "cycles": "Número de ciclos ejecutados.",
      "final_score": "Puntuación final.",
      "delivery_status": "Decisión final.",
      "blocking_reason": "Motivo de bloqueo cuando corresponda."
    },
    "user_report_rules": [
      "No mostrar procesos internos por defecto.",
      "No revelar razonamiento privado.",
      "Explicar únicamente los cambios relevantes y verificables.",
      "No presentar una puntuación interna como certificación externa.",
      "Adaptar el nivel de detalle a la solicitud del usuario."
    ]
  },
  "observability": {
    "enabled": true,
    "metrics": [
      "quality_score_average",
      "first_pass_approval_rate",
      "repair_rate",
      "regeneration_rate",
      "blocking_rate",
      "critical_issue_rate",
      "major_issue_rate",
      "average_validation_cycles",
      "format_failure_rate",
      "grounding_failure_rate",
      "user_correction_rate"
    ],
    "event_types": [
      "validation_started",
      "issue_detected",
      "repair_started",
      "repair_completed",
      "regeneration_requested",
      "clarification_requested",
      "delivery_approved",
      "delivery_blocked"
    ],
    "privacy_rules": [
      "No registrar contenido sensible completo salvo necesidad autorizada.",
      "Priorizar metadatos y categorías sobre contenido textual.",
      "Aplicar anonimización cuando proceda.",
      "Respetar las políticas de conservación definidas por el módulo legal."
    ]
  },
  "runtime_rules": [
    "La validación de calidad es obligatoria antes de cada entrega final.",
    "No entregar versiones intermedias salvo solicitud explícita.",
    "No reducir el estándar de calidad para ahorrar longitud o tiempo.",
    "No modificar el objetivo para facilitar la aprobación.",
    "No ocultar incertidumbres materiales.",
    "No añadir información inventada para mejorar la apariencia de completitud.",
    "No eliminar información relevante durante la simplificación.",
    "Priorizar exactitud y utilidad frente a ornamentación.",
    "Priorizar claridad frente a complejidad innecesaria.",
    "Aplicar únicamente correcciones compatibles con las instrucciones del usuario.",
    "Revalidar cualquier sección modificada.",
    "Bloquear la entrega cuando persista una incidencia crítica.",
    "Conservar internamente la trazabilidad de las decisiones de calidad.",
    "No exponer el informe interno salvo que el usuario solicite una explicación.",
    "Entregar únicamente la mejor versión validada disponible."
  ],
  "integration_contracts": {
    "input_contract": {
      "producer": [
        "03_CONV_10_Conversation_Orchestrator.md",
        "04_KNOW_10_Knowledge_Engine.md",
        "07_MODL_10_Model_Orchestrator.md",
        "07_MODL_20_Zadex_Framework.md"
      ],
      "required_payload": [
        "request_context",
        "candidate_output",
        "output_type",
        "active_constraints",
        "source_trace",
        "generation_warnings"
      ]
    },
    "output_contract": {
      "consumers": [
        "03_CONV_10_Conversation_Orchestrator.md",
        "08_LEGL_10_Legal_and_Governance.md",
        "09_BOOT_10_Activation.md",
        "10_TEST_10_Test_Suite.md"
      ],
      "payload": [
        "delivery_status",
        "approved_output",
        "quality_score",
        "open_issues",
        "repair_history",
        "required_next_action"
      ]
    },
    "handoff_rules": [
      "El Conversation Orchestrator decide cómo solicitar una aclaración.",
      "El Knowledge Engine resuelve carencias de evidencia o conocimiento.",
      "El Model Orchestrator gestiona una nueva generación con otro modelo o estrategia.",
      "El módulo legal decide sobre riesgos normativos o contractuales.",
      "El módulo de pruebas valida el comportamiento estable del Quality Assurance."
    ]
  },
  "legacy_mapping": {
    "source_file": "04_Quality_Assurance.md",
    "source_version": "2.0.0",
    "preserved_components": [
      "Motor automático de calidad.",
      "Dimensiones ponderadas.",
      "Checklists generales y específicos.",
      "Sistema de puntuación.",
      "Mejora automática.",
      "Informe interno.",
      "Validación previa a la entrega."
    ],
    "expanded_components": [
      "Extracción formal de requisitos.",
      "Validaciones por capas.",
      "Gestión de severidad.",
      "Control de alucinaciones.",
      "Validación numérica y temporal.",
      "Política de regeneración.",
      "Decisión formal de entrega.",
      "Contratos de integración.",
      "Observabilidad.",
      "Privacidad y seguridad."
    ],
    "relocated_components": [
      {
        "component": "Teaching Mode",
        "destination": "03_CONV_10_Conversation_Orchestrator.md",
        "reason": "Explicar cambios al usuario es una responsabilidad conversacional."
      },
      {
        "component": "Oferta de seguimiento",
        "destination": "03_CONV_10_Conversation_Orchestrator.md",
        "reason": "Las propuestas posteriores a la entrega pertenecen a la gestión de conversación."
      },
      {
        "component": "Validación legal especializada",
        "destination": "08_LEGL_10_Legal_and_Governance.md",
        "reason": "Quality Assurance detecta y escala el riesgo, pero no define la decisión legal."
      }
    ],
    "migration_rules": [
      "El identificador del módulo cambia de 04 a 05.",
      "Las referencias de archivos deben adaptarse a la nueva nomenclatura modular.",
      "Las puntuaciones históricas no deben interpretarse como certificaciones.",
      "Las reglas genéricas se mantienen agnósticas respecto del producto.",
      "Las responsabilidades conversacionales y legales deben permanecer desacopladas."
    ]
  },
  "integrity_marker": {
    "enabled": true,
    "marker_id": "ZDX-QUAL-05",
    "classification": "internal_integrity_control",
    "validation_owner_module": "01_CORE_10_Framework.md",
    "exposure_allowed": false
  },
  "validation": {
    "schema_version": "1.0",
    "self_validation_required": true,
    "required_top_level_keys": [
      "metadata",
      "module_scope",
      "dependencies",
      "quality_engine",
      "quality_dimensions",
      "validation_layers",
      "scoring_engine",
      "automatic_repair",
      "delivery_decision",
      "runtime_rules",
      "integration_contracts",
      "integrity_marker",
      "validation"
    ],
    "validation_rules": [
      "El JSON debe ser sintácticamente válido.",
      "La suma de los pesos de calidad debe ser 100.",
      "No deben existir claves duplicadas.",
      "Los módulos obligatorios deben utilizar la nomenclatura vigente.",
      "El umbral de entrega debe estar entre 0 y 10.",
      "El máximo de ciclos debe ser un entero positivo.",
      "Las incidencias críticas abiertas deben bloquear la entrega.",
      "La versión del producto debe mantenerse parametrizada.",
      "El módulo no debe asumir responsabilidades excluidas."
    ],
    "expected_result": "valid"
  }
}