{
  "metadata": {
    "module_id": "08_LEGL_10",
    "module_code": "LEGL",
    "module_name": "Legal and Governance",
    "file_name": "08_LEGL_10_Legal_and_Governance.md",
    "module_type": "legal_governance_and_compliance",
    "framework_name": "Zadex AI Framework",
    "framework_version": "{{FRAMEWORK_VERSION}}",
    "product_name": "{{PRODUCT_NAME}}",
    "product_version": "{{PRODUCT_VERSION}}",
    "owner": "Jairo García",
    "organization": "Zadex",
    "status": "active",
    "language": "es-ES",
    "description": "Módulo responsable del gobierno, cumplimiento normativo, privacidad, seguridad, gestión de riesgos, auditoría y aplicación de políticas del Zadex AI Framework."
  },
  "module_scope": {
    "purpose": "Garantizar que cualquier ejecución del framework respete la legislación aplicable, las políticas corporativas, los requisitos de privacidad, seguridad, gobierno del dato y uso responsable de la inteligencia artificial.",
    "responsibilities": [
      "Aplicar políticas legales.",
      "Aplicar políticas de privacidad.",
      "Aplicar controles de seguridad.",
      "Gestionar clasificación de datos.",
      "Controlar permisos de ejecución.",
      "Evaluar riesgos regulatorios.",
      "Aplicar restricciones geográficas.",
      "Controlar tratamiento de información sensible.",
      "Gestionar auditoría y trazabilidad.",
      "Aplicar principios de IA responsable.",
      "Evaluar acciones con efectos externos.",
      "Coordinar revisiones humanas obligatorias.",
      "Gestionar políticas de retención.",
      "Aplicar gobierno del framework."
    ],
    "excluded_responsibilities": [
      "Interpretar la intención del usuario.",
      "Seleccionar modelos.",
      "Redactar respuestas.",
      "Aplicar la identidad de marca.",
      "Realizar búsquedas de conocimiento.",
      "Validar calidad lingüística.",
      "Gestionar interfaces de usuario.",
      "Implementar infraestructura.",
      "Sustituir el asesoramiento jurídico humano.",
      "Resolver conflictos legales complejos sin revisión."
    ]
  },
  "dependencies": {
    "required_modules": [
      "01_CORE_10_Framework.md",
      "02_BUSI_10_Product_Configuration.md",
      "03_CONV_10_Conversation_Orchestrator.md"
    ],
    "optional_modules": [
      "04_KNOW_10_Knowledge_Engine.md",
      "05_QUAL_10_Quality_Assurance.md",
      "06_BRND_10_Zadex_DNA.md",
      "07_MODL_10_Model_Orchestrator.md",
      "07_MODL_20_Zadex_Framework.md",
      "09_BOOT_10_Activation.md",
      "10_TEST_10_Test_Suite.md"
    ],
    "execution_position": "cross_cutting_governance_layer",
    "dependency_rules": [
      "Puede intervenir antes, durante y después de cualquier ejecución.",
      "Tiene prioridad sobre cualquier configuración funcional.",
      "Puede bloquear modelos, herramientas o acciones.",
      "Puede exigir revisión humana.",
      "Debe registrar toda decisión de gobierno relevante.",
      "No puede modificar el objetivo legítimo del usuario salvo obligación legal."
    ]
  },
  "governance_principles": {
    "principles": [
      {
        "id": "lawfulness",
        "name": "Legalidad",
        "description": "Toda ejecución debe respetar la legislación aplicable."
      },
      {
        "id": "privacy",
        "name": "Privacidad",
        "description": "Los datos personales deben protegerse durante todo su ciclo de vida."
      },
      {
        "id": "security",
        "name": "Seguridad",
        "description": "La información debe mantenerse protegida frente a accesos y usos no autorizados."
      },
      {
        "id": "accountability",
        "name": "Responsabilidad",
        "description": "Las decisiones relevantes deben ser auditables."
      },
      {
        "id": "transparency",
        "name": "Transparencia",
        "description": "Las limitaciones y actuaciones relevantes deben poder justificarse."
      },
      {
        "id": "proportionality",
        "name": "Proporcionalidad",
        "description": "Los controles deben ser proporcionales al riesgo."
      },
      {
        "id": "data_minimization",
        "name": "Minimización",
        "description": "Solo debe procesarse la información estrictamente necesaria."
      },
      {
        "id": "human_oversight",
        "name": "Supervisión humana",
        "description": "Las decisiones críticas deben poder revisarse por personas."
      },
      {
        "id": "least_privilege",
        "name": "Mínimo privilegio",
        "description": "Cada componente debe disponer únicamente de los permisos necesarios."
      },
      {
        "id": "default_secure",
        "name": "Seguro por defecto",
        "description": "Ante la duda, debe prevalecer la opción más segura."
      }
    ],
    "priority_order": [
      "legal_compliance",
      "human_safety",
      "privacy",
      "security",
      "user_intent",
      "business_objectives",
      "performance",
      "cost"
    ]
  },
  "jurisdiction_management": {
    "enabled": true,
    "supported_modes": [
      "global_default",
      "country_profile",
      "regional_profile",
      "customer_specific",
      "tenant_specific"
    ],
    "jurisdiction_schema": {
      "jurisdiction_id": "Identificador.",
      "country": "País.",
      "region": "Región.",
      "applicable_laws": "Normativa aplicable.",
      "privacy_requirements": "Requisitos de privacidad.",
      "retention_policy": "Retención.",
      "data_transfer_rules": "Transferencias internacionales.",
      "restricted_capabilities": "Capacidades limitadas.",
      "mandatory_disclosures": "Avisos obligatorios.",
      "human_review_rules": "Revisión humana.",
      "effective_date": "Fecha de aplicación."
    },
    "rules": [
      "Toda ejecución debe asociarse a un perfil jurisdiccional.",
      "La jurisdicción puede depender del cliente, del dato o del procesamiento.",
      "Las restricciones territoriales prevalecen sobre preferencias del producto.",
      "Las políticas deben poder coexistir cuando intervengan varias jurisdicciones.",
      "Las jurisdicciones deben versionarse."
    ]
  },
  "data_classification": {
    "classification_levels": [
      {
        "id": "public",
        "description": "Información pública."
      },
      {
        "id": "internal",
        "description": "Información de uso interno."
      },
      {
        "id": "confidential",
        "description": "Información confidencial."
      },
      {
        "id": "restricted",
        "description": "Información altamente restringida."
      }
    ],
    "classification_rules": [
      "Toda entrada debe clasificarse.",
      "La clasificación puede heredarse del origen.",
      "La clasificación puede elevarse durante la ejecución.",
      "Nunca debe reducirse automáticamente.",
      "La clasificación condiciona modelos, herramientas y almacenamiento."
    ]
  },
  "privacy_management": {
    "privacy_principles": [
      "data_minimization",
      "purpose_limitation",
      "storage_limitation",
      "accuracy",
      "integrity",
      "confidentiality",
      "accountability"
    ],
    "personal_data_categories": [
      "basic_identity",
      "contact_information",
      "financial_data",
      "health_data",
      "employment_data",
      "government_identifiers",
      "biometric_data",
      "location_data",
      "behavioral_data",
      "sensitive_personal_data"
    ],
    "privacy_controls": [
      "masking",
      "pseudonymization",
      "anonymization",
      "redaction",
      "tokenization",
      "field_filtering",
      "purpose_validation"
    ],
    "rules": [
      "No enviar datos innecesarios a modelos externos.",
      "Anonimizar siempre que sea viable.",
      "Aplicar minimización antes del procesamiento.",
      "Los datos sensibles requieren controles reforzados.",
      "La finalidad debe ser compatible con el tratamiento."
    ]
  },
  "security_management": {
    "security_domains": [
      "identity",
      "authentication",
      "authorization",
      "data_protection",
      "network",
      "application",
      "audit",
      "secrets_management",
      "incident_management"
    ],
    "security_controls": [
      "least_privilege",
      "role_based_access",
      "attribute_based_access",
      "credential_isolation",
      "encrypted_transport",
      "encrypted_storage",
      "audit_logging",
      "tamper_detection",
      "key_rotation",
      "secret_vault"
    ],
    "rules": [
      "Las credenciales nunca deben formar parte del prompt.",
      "Las claves deben almacenarse en sistemas seguros.",
      "Toda comunicación sensible debe utilizar transporte cifrado.",
      "Los permisos deben evaluarse antes de cualquier acción externa.",
      "Los eventos de seguridad deben registrarse."
    ]
  },
  "ai_governance": {
    "principles": [
      "fairness",
      "robustness",
      "human_control",
      "explainability",
      "traceability",
      "accountability",
      "risk_management",
      "continuous_monitoring"
    ],
    "governance_requirements": [
      "Evaluar riesgos.",
      "Documentar decisiones relevantes.",
      "Permitir auditoría.",
      "Mantener supervisión humana.",
      "Controlar cambios.",
      "Gestionar incidencias.",
      "Versionar políticas.",
      "Evaluar impacto."
    ],
    "rules": [
      "La IA debe permanecer bajo responsabilidad humana.",
      "Los cambios relevantes deben ser auditables.",
      "Las decisiones automáticas críticas deben poder revisarse.",
      "Las limitaciones conocidas deben documentarse."
    ]
  },
  "risk_management": {
    "risk_levels": [
      "low",
      "medium",
      "high",
      "critical"
    ],
    "risk_dimensions": [
      "legal",
      "privacy",
      "security",
      "financial",
      "operational",
      "reputational",
      "ethical",
      "ai_specific"
    ],
    "risk_actions": {
      "low": [
        "continue"
      ],
      "medium": [
        "additional_validation"
      ],
      "high": [
        "quality_review",
        "policy_review"
      ],
      "critical": [
        "human_review",
        "execution_block"
      ]
    },
    "rules": [
      "El riesgo debe calcularse antes de ejecutar acciones externas.",
      "El riesgo puede aumentar durante la ejecución.",
      "La clasificación de riesgo debe conservarse en la trazabilidad.",
      "Los riesgos críticos requieren aprobación explícita."
    ]
  },
  "human_review": {
    "mandatory_conditions": [
      "critical_risk",
      "legal_uncertainty",
      "external_irreversible_action",
      "high_financial_impact",
      "high_regulatory_impact",
      "customer_policy_requirement",
      "explicit_framework_policy"
    ],
    "review_levels": [
      "recommended",
      "required",
      "mandatory_before_execution"
    ],
    "rules": [
      "Las revisiones deben registrar responsable y decisión.",
      "Las aprobaciones deben ser trazables.",
      "La revisión no sustituye los controles automáticos.",
      "El framework debe poder suspender la ejecución mientras espera revisión."
    ]
  },
  "policy_engine": {
    "enabled": true,
    "policy_types": [
      "legal_policy",
      "privacy_policy",
      "security_policy",
      "product_policy",
      "tenant_policy",
      "customer_policy",
      "runtime_policy"
    ],
    "evaluation_order": [
      "core_non_overridable",
      "legal",
      "security",
      "tenant",
      "customer",
      "product",
      "runtime"
    ],
    "policy_results": [
      "allow",
      "allow_with_conditions",
      "require_review",
      "deny"
    ],
    "rules": [
      "Toda política debe estar versionada.",
      "Las políticas superiores prevalecen.",
      "Las decisiones deben ser explicables.",
      "Las políticas deben ser deterministas."
    ]
  },
  "audit_management": {
    "enabled": true,
    "audit_events": [
      "policy_evaluation",
      "human_review",
      "permission_check",
      "provider_selection",
      "external_action",
      "model_execution",
      "knowledge_access",
      "security_event",
      "configuration_change",
      "framework_activation"
    ],
    "audit_record": {
      "audit_id": "Identificador único.",
      "timestamp": "Fecha y hora.",
      "actor": "Usuario, módulo o sistema.",
      "action": "Acción realizada.",
      "resource": "Recurso afectado.",
      "decision": "Resultado.",
      "reason": "Justificación.",
      "risk_level": "Nivel de riesgo.",
      "policy_version": "Versión aplicada.",
      "trace_id": "Traza asociada."
    },
    "rules": [
      "Toda decisión relevante debe generar auditoría.",
      "La auditoría debe ser inmutable.",
      "Las evidencias deben mantenerse conforme a la política de retención.",
      "La auditoría no debe almacenar datos innecesarios."
    ]
  },
  "retention_management": {
    "enabled": true,
    "retention_profiles": [
      "temporary",
      "standard",
      "extended",
      "legal_hold"
    ],
    "retention_rules": [
      "La retención depende de la jurisdicción y del cliente.",
      "Los datos deben eliminarse al finalizar el periodo aplicable.",
      "Las retenciones legales prevalecen sobre cualquier otra política.",
      "Los registros eliminados deben dejar evidencia de la operación."
    ]
  },
  "external_action_governance": {
    "enabled": true,
    "protected_actions": [
      "send_email",
      "calendar_modification",
      "database_update",
      "payment_execution",
      "document_signature",
      "crm_update",
      "erp_update",
      "external_api_call",
      "file_deletion",
      "automation_execution"
    ],
    "authorization_levels": [
      "automatic",
      "user_confirmation",
      "human_approval",
      "administrator_only"
    ],
    "rules": [
      "Toda acción irreversible debe validarse antes de ejecutarse.",
      "Las acciones financieras requieren controles reforzados.",
      "Las acciones externas deben registrar resultado y evidencias.",
      "La autorización debe comprobarse inmediatamente antes de ejecutar."
    ]
  },
  "regional_processing": {
    "enabled": true,
    "processing_modes": [
      "global",
      "regional",
      "country_only",
      "customer_hosted",
      "private_infrastructure"
    ],
    "rules": [
      "El procesamiento debe respetar restricciones territoriales.",
      "Los modelos no autorizados por región no pueden utilizarse.",
      "Las transferencias internacionales deben quedar registradas.",
      "La residencia del dato prevalece sobre preferencias de rendimiento."
    ]
  },
  "provider_governance": {
    "provider_requirements": [
      "approved_contract",
      "security_assessment",
      "privacy_assessment",
      "technical_validation",
      "business_owner",
      "risk_acceptance"
    ],
    "provider_rules": [
      "Solo pueden utilizarse proveedores aprobados.",
      "Los proveedores deben reevaluarse periódicamente.",
      "Los cambios de capacidades relevantes requieren revisión.",
      "Las restricciones contractuales deben incorporarse al framework."
    ]
  },
  "compliance_monitoring": {
    "enabled": true,
    "monitoring_dimensions": [
      "policy_compliance",
      "security_compliance",
      "privacy_compliance",
      "runtime_compliance",
      "model_compliance",
      "provider_compliance"
    ],
    "actions": [
      "alert",
      "review",
      "block_execution",
      "increase_logging",
      "request_human_review"
    ],
    "rules": [
      "El incumplimiento crítico debe bloquear la ejecución.",
      "Las desviaciones menores deben registrarse.",
      "Los indicadores deben revisarse periódicamente.",
      "Las acciones correctivas deben ser trazables."
    ]
  },
  "incident_management": {
    "incident_levels": [
      "informational",
      "minor",
      "major",
      "critical"
    ],
    "incident_categories": [
      "privacy",
      "security",
      "availability",
      "compliance",
      "provider",
      "quality",
      "operational"
    ],
    "incident_workflow": [
      "detect",
      "classify",
      "contain",
      "investigate",
      "resolve",
      "review",
      "close"
    ],
    "rules": [
      "Todo incidente debe disponer de identificador único.",
      "Los incidentes críticos requieren escalado inmediato.",
      "Las acciones correctivas deben registrarse.",
      "La resolución debe incorporar lecciones aprendidas."
    ]
  },
  "documentation_requirements": {
    "required_documents": [
      "framework_policies",
      "privacy_policy",
      "security_policy",
      "risk_register",
      "model_registry",
      "provider_registry",
      "audit_policy",
      "retention_policy",
      "incident_policy"
    ],
    "rules": [
      "Toda política debe estar documentada.",
      "Los documentos deben versionarse.",
      "Las modificaciones deben ser aprobadas.",
      "La documentación debe mantenerse sincronizada con el framework."
    ]
  },
  "integration_contracts": {
    "input_contract": {
      "required": [
        "request_context",
        "risk_profile",
        "jurisdiction_profile",
        "product_configuration"
      ]
    },
    "output_contract": {
      "provides": [
        "policy_decision",
        "legal_constraints",
        "security_constraints",
        "privacy_constraints",
        "human_review_requirement"
      ]
    },
    "handoff_rules": [
      "Conversation Orchestrator recibe restricciones aplicables.",
      "Model Orchestrator aplica limitaciones técnicas.",
      "Quality Assurance incorpora resultados legales en la validación.",
      "Activation valida políticas antes de activar."
    ]
  },
  "runtime_rules": [
    "Las políticas legales prevalecen sobre cualquier configuración funcional.",
    "Toda ejecución debe disponer de un perfil jurisdiccional.",
    "Los datos personales deben minimizarse.",
    "Las acciones externas requieren autorización suficiente.",
    "Toda decisión crítica debe ser trazable.",
    "Las revisiones humanas no pueden omitirse cuando sean obligatorias.",
    "Los proveedores deben cumplir las políticas aprobadas.",
    "Las restricciones territoriales deben respetarse.",
    "El framework debe permanecer auditable.",
    "La seguridad debe aplicarse por defecto."
  ],
  "legacy_mapping": {
    "new_module": "08_LEGL_10_Legal_and_Governance.md",
    "migration_objective": "Centralizar todas las capacidades de gobierno, cumplimiento, privacidad, seguridad y auditoría del Zadex AI Framework.",
    "migrated_capabilities": [
      "Políticas.",
      "Privacidad.",
      "Seguridad.",
      "Clasificación del dato.",
      "Gestión de riesgos.",
      "Auditoría.",
      "Retención.",
      "Revisión humana.",
      "Gobierno de proveedores.",
      "Cumplimiento."
    ],
    "future_extensions": [
      "EU AI Act profiles.",
      "ISO 42001 mappings.",
      "NIST AI RMF mappings.",
      "Regulatory monitoring automation."
    ]
  },
  "integrity_marker": {
    "enabled": true,
    "marker_id": "ZDX-LEGL-08",
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
      "governance_principles",
      "privacy_management",
      "security_management",
      "policy_engine",
      "runtime_rules",
      "integrity_marker",
      "validation"
    ],
    "validation_rules": [
      "El JSON debe ser válido.",
      "No deben existir claves duplicadas.",
      "Las políticas superiores deben prevalecer sobre las inferiores.",
      "Toda acción externa debe poder evaluarse mediante políticas.",
      "Toda decisión crítica debe generar auditoría.",
      "Las clasificaciones de datos deben ser consistentes.",
      "Las jurisdicciones deben estar correctamente versionadas.",
      "El módulo no debe asumir responsabilidades funcionales de otros módulos."
    ],
    "expected_result": "valid"
  }
}