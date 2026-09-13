# Deciciones de CObertura

## Riesgos que se probarán primero
1. **R1 - Fallo en el registro de orden tras pago aprobado:** Pruebas de integración entre Checkout y confirmación de BD.
2. **R2 - Inconsistencia de inventario entre Web y API:** Validaciones cruzadas de Endpoints API vs interfaz Web.
3. **R3 - Exposición de datos de usuario:** Pruebas funcionales de autenticación, logout y manejo de sesión.

## ¿Por qué esos riesgos son prioridad?
Porque afectan directamente los ingresos del negocio (conversión y pagos), la integridad del inventario y la seguridad del cliente. Priorizar el testing basado en riesgos financieros evita incidentes graves en producción.

## Qué se probará menos o quedará fuera por ahora
- **Pruebas de compatibilidad móvil extensiva (R5):** Pruebas en dispositivos o pantallas antiguas.
- **Automatización de catálogo secundario:** Navegación exploratoria no transaccional.
- **Pruebas de estrés masivo a la API:** Enfocadas solo a flujos CRUD funcionales en esta fase.

## Justificación de exclusiones
Dada la restricción de tiempo (60 min), la estrategia debe priorizar transacciones críticas. Los fallos estéticos o la falta de soporte en navegadores obsoletos no detienen las operaciones transaccionales clave.