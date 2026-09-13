# Risk Matrix

| ID | Riesgo | Impacto | Probabilidad | Nivel | Justificación |
|---|---|---|---|---|---|
| R1 | Procesamiento de cobro aprobado en pasarela pero la orden falla en registrarse en base de datos. | Alto | Alta | Crítico | Pérdida directa de dinero e inconsistencia legal/financiera para el usuario y negocio. |
| R2 | Inconsistencia de datos entre el inventario de la API y el stock visible en la App Web. | Alto | Media | Alto | Provoca ventas de productos sin stock real, afectando la logística y la reputación. |
| R3 | Sesión de usuario expuesta por falta de expiración o desprotección de datos de credenciales. | Alto | Media | Alto | Compromete la privacidad del usuario y puede derivar en fallos de seguridad graves. |
| R4 | Falla al calcular el precio total del carrito al modificar o ingresar cantidades negativas o nulas. | Medio | Media | Medio | Permite compras por montos erróneos o bloquea la conversión del carrito. |
| R5 | Desalineación visual de elementos del catálogo en resoluciones móviles específicas. | Bajo | Media | Bajo | Afecta la estética de la app pero no impide que el usuario complete la compra. |