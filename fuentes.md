# Fuentes y Metodología

Este documento detalla las fuentes de datos utilizadas en el análisis de costos de la licitación del software del Hospital de Ñuble.

## Fuente Principal

**Licitación ID: 1057898-8-LR26**
- **Título**: "Adquisición de Softwares para el Nuevo Hospital Regional de Ñuble"
- **Organismo**: Servicio de Salud Ñuble
- **Portal**: Mercado Público (Chile)
- **URL**: https://www.mercadopublico.cl/Procurement/Modules/RFB/DetailsAcquisition.aspx?idlicitacion=1057898-8-LR26
- **Monto estimado**: $14.801.350.000 CLP
- **Fecha de publicación**: 29/01/2026
- **Fecha de cierre**: 12/03/2026

## Fuentes de Datos Comparativos

### 1. CESFAM (Centros de Salud Familiar)

**Nota**: Las cifras utilizadas para CESFAM Grande ($9.800.000.000) y CESFAM Standard ($6.400.000.000) fueron proporcionadas por el usuario del proyecto y requieren verificación contra fuentes oficiales.

**Fuentes sugeridas para verificación**:
- Presupuestos del Ministerio de Salud de Chile (MINSAL)
- Licitaciones de construcción de CESFAM en portal Mercado Público
- Estudios de costos de infraestructura sanitaria del Departamento de Inversiones del MINSAL

### 2. Costo de Cirugías

**Cifra utilizada**: $1.450.000 CLP por cirugía

**Fuente requerida**: Esta cifra necesita ser validada contra:
- Aranceles FONASA para procedimientos quirúrgicos
- Costos promedio publicados por MINSAL
- Estudios de costos hospitalarios del Departamento de Estadísticas e Información de Salud (DEIS)

**Recomendación**: Solicitar a MINSAL el costo promedio ponderado de cirugías electivas en hospitales públicos regionales.

### 3. Déficit de Salud en Tarapacá

**Cifra utilizada**: $14.000.000.000 CLP

**Fuente requerida**: Esta cifra debe ser verificada contra:
- Informes de déficit presupuestario del Servicio de Salud Tarapacá
- Cuenta Pública del MINSAL
- Informes de la Contraloría General de la República sobre ejecución presupuestaria en salud

### 4. Máquinas de Resonancia Magnética (MRI)

**Cifra utilizada**: $1.500.000.000 CLP por equipo

**Fuentes sugeridas para verificación**:
- Licitaciones de equipamiento médico en portal Mercado Público
- Precio de referencia de equipos Siemens, GE Healthcare, Philips en licitaciones públicas chilenas
- Estudios de costos de tecnología médica del MINSAL

**Ejemplo de búsqueda en Mercado Público**:
```
Palabras clave: "resonancia magnética", "MRI", "equipo resonador"
Filtros: Organismo público de salud, últimos 24 meses
```

### 5. Costo Salud per Cápita

**Cifra utilizada**: $11.205 CLP

**Fuente requerida**: 
- FONASA: Costo promedio de atención ambulatoria per cápita
- MINSAL: Estadísticas de gasto en salud por beneficiario
- Superintendencia de Salud: Informes de costos de prestaciones

**Cálculo sugerido**: Gasto total en salud pública / población beneficiaria anual

## Precedentes Internacionales de Fracasos en Software Hospitalario

### 1. UK NHS National Programme for IT

**Fuentes académicas y oficiales**:
- National Audit Office (NAO). (2011). "The National Programme for IT in the NHS: An Update on the Delivery of Detailed Care Records Systems"
- House of Commons Committee of Public Accounts. (2011). "The National Programme for IT in the NHS: an update on the delivery of detailed care records systems"
- Monto: £10.000 millones (aproximadamente)
- Resultado: Proyecto cancelado en 2011

**Referencias**:
- https://www.nao.org.uk/reports/the-national-programme-for-it-in-the-nhs-an-update-on-the-delivery-of-detailed-care-records-systems/

### 2. Queensland Health Payroll System (Australia)

**Fuentes oficiales**:
- Queensland Audit Office reports on the Health Payroll System
- Queensland Government Commission of Inquiry (2013)
- Sobrecosto: AU$1.200 millones aproximadamente
- Años: 2010-2013

**Referencias**:
- Queensland Commission of Inquiry reports (disponible en archivos del gobierno de Queensland)

### 3. Epic Systems Implementation Costs

**Fuentes de la industria**:
- KLAS Research: Informes de satisfacción y costos de implementación de EMR
- HIMSS Analytics: Estudios de costos de sistemas de información hospitalaria
- Artículos académicos en Journal of the American Medical Informatics Association (JAMIA)

**Nota**: Los sobrecostos del 30-50% son estimaciones basadas en múltiples casos reportados en la literatura de informática médica.

## Estándares Técnicos Mencionados

### HL7 FHIR (Fast Healthcare Interoperability Resources)
- **Organismo**: Health Level Seven International
- **Website**: https://www.hl7.org/fhir/
- **Descripción**: Estándar de interoperabilidad para intercambio de datos de salud

### DICOM (Digital Imaging and Communications in Medicine)
- **Organismo**: DICOM Standards Committee
- **Website**: https://www.dicomstandard.org/
- **Descripción**: Estándar para manejo de imágenes médicas

## Metodología de Cálculo

### Cálculo de "Total Posible"

La columna "Total Posible" en el CSV representa cuántas unidades de cada alternativa se podrían financiar con el presupuesto del software:

```
Total Posible = Monto Software / Costo Unitario de Alternativa
Total Posible = $14.801.350.000 / Costo de Item
```

**Ejemplos**:
- CESFAM Grande: $14.801.350.000 / $9.800.000.000 = 1,51 ≈ 1,5 centros
- Cirugías: $14.801.350.000 / $1.450.000 = 10.207,83 ≈ 10.208 cirugías
- MRI: $14.801.350.000 / $1.500.000.000 = 9,87 ≈ 10 máquinas

### Cálculo de Porcentajes en Visualización

Los porcentajes mostrados en la visualización web representan:

**Costo unitario (%)**:
```
(Costo Unitario / Monto Software) × 100
```

**Costo total (%)**:
```
(Costo Unitario × Cantidad × / Monto Software) × 100
```

## Limitaciones y Advertencias

⚠️ **IMPORTANTE**: Muchas de las cifras comparativas utilizadas en este análisis fueron proporcionadas por el usuario y **requieren verificación contra fuentes oficiales** antes de publicación periodística.

### Datos que DEBEN ser verificados:

1. ✅ **Verificado**: Monto y datos de la licitación (fuente: Mercado Público)
2. ⚠️ **Requiere verificación**: Costo de CESFAM Grande y Standard
3. ⚠️ **Requiere verificación**: Costo promedio de cirugías
4. ⚠️ **Requiere verificación**: Déficit de Salud en Tarapacá
5. ⚠️ **Requiere verificación**: Costo de equipos MRI
6. ⚠️ **Requiere verificación**: Costo per cápita de atención

### Recomendaciones para Verificación

1. **Contactar directamente**:
   - Departamento de Prensa MINSAL
   - Departamento de Inversiones MINSAL
   - Servicio de Salud Ñuble
   - Servicio de Salud Tarapacá

2. **Solicitar por Ley de Transparencia**:
   - Costos de construcción de CESFAM (últimos 5 años)
   - Costos de adquisición de equipamiento médico mayor
   - Presupuestos de déficit por servicio de salud

3. **Revisar en Mercado Público**:
   - Licitaciones adjudicadas de infraestructura sanitaria
   - Licitaciones de equipamiento médico
   - Comparar montos históricos

## Actualizaciones

**Última revisión**: Febrero 2026

**Versión**: 1.0

**Mantenedor**: [Tu nombre/organización]

---

## Notas para Periodistas

Si va a utilizar estas cifras en una publicación:

1. **Cite siempre la fuente primaria** (Mercado Público para la licitación)
2. **Verifique independientemente** las cifras comparativas antes de publicar
3. **Use lenguaje condicional** para datos no verificados ("según estimaciones", "cifras aproximadas")
4. **Contacte a las fuentes oficiales** para obtener confirmación
5. **Documente sus solicitudes** de información pública

## Contacto para Correcciones

Si detecta errores en estas fuentes o tiene acceso a datos oficiales actualizados, por favor contactar a: [tu email]