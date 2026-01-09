# Aplicación Móvil

La aplicación móvil de GMAS Estados de Cuenta BC permite a los usuarios consultar estados de cuenta de forma rápida y segura desde dispositivos móviles (iOS y Android).

## Características Principales

- **Acceso Seguro**: Autenticación con usuario/contraseña y multi-factor
- **Multiempresa**: Selección de empresa para consultas específicas
- **Consulta de Estados**: Visualización detallada de estados de cuenta
- **KPIs en Tiempo Real**: Métricas y estadísticas actualizadas
- **Análisis de Datos**: Sumatoria y análisis de registros seleccionados
- **Interfaz Intuitiva**: Diseño responsive y fácil de usar

## Inicio de Sesión

![Login](/img/app-mobil/login.png)

La pantalla de inicio de sesión permite el acceso a la aplicación:

### Credenciales

- **Usuario**: Nombre de usuario o correo electrónico
- **Contraseña**: Contraseña de acceso

### Funcionalidades

- **Recordar Usuario**: Guardar usuario para futuros accesos
- **Recuperar Contraseña**: Enlace para restablecer contraseña
- **Validación**: Verificación de credenciales en tiempo real

### Seguridad

- Conexión segura mediante HTTPS
- Encriptación de credenciales
- Límite de intentos fallidos
- Cierre automático de sesión por inactividad

## Autenticación Multi-Factor (MFA)

![Multi-Factor Authentication](/img/app-mobil/multi-factor.png)

Capa adicional de seguridad mediante autenticación de dos factores:

### Métodos de Verificación

- **Código por Email**: Envío de código al correo electrónico

### Proceso de Verificación

1. Ingresar usuario y contraseña
2. Seleccionar método de verificación
3. Recibir código de seguridad
4. Ingresar código en la aplicación
5. Acceder al sistema


## Selección de Empresa

![Seleccionar Empresa](/img/app-mobil/selecciona-empresa.png)

Después de la autenticación, se presenta la selección de empresa:

### Funcionalidades

- **Listado de Empresas**: Todas las compañías asignadas al usuario
- **Búsqueda**: Campo para filtrar empresas por nombre
- **Empresa por Defecto**: Marcador de empresa principal
- **Información de Empresa**: Nombre, código y estado
- **Selección Rápida**: Acceso directo con un toque

### Características

- **Vista de Tarjetas**: Presentación visual clara
- **Indicadores de Estado**: Empresas activas/inactivas
- **Acceso Rápido**: Recordar última empresa seleccionada
- **Cambio de Empresa**: Posibilidad de cambiar sin cerrar sesión

### Permisos

El listado muestra únicamente las empresas a las que el usuario tiene acceso autorizado según sus permisos configurados en el sistema.

## KPIs y Estados de Cuenta

![KPIs Estado de Cuenta](/img/app-mobil/kpi-estado-cuenta.png)

Panel principal con métricas y estadísticas clave:

### Indicadores Principales

#### Métricas Financieras

- **Saldo Total**: Balance general de la cuenta
- **Saldo Vencido**: Montos pendientes de pago
- **Saldo por Vencer**: Compromisos próximos a vencer
- **Crédito Disponible**: Límite de crédito disponible
- **Días Promedio de Pago**: Indicador de comportamiento

#### Indicadores de Desempeño

- **Pedidos del Mes**: Cantidad y monto
- **Última Compra**: Fecha y monto
- **Ticket Promedio**: Valor promedio de transacciones
- **Tendencia**: Comparativa con períodos anteriores

### Visualización

- **Gráficas**: Representación visual de tendencias
- **Comparativas**: Mes actual vs anterior
- **Alertas**: Indicadores de saldos vencidos o límites excedidos
- **Código de Colores**: Verde (favorable), Amarillo (atención), Rojo (crítico)

### Actualización

- **Tiempo Real**: Datos actualizados automáticamente
- **Última Actualización**: Timestamp de sincronización
- **Sincronización Manual**: Opción de actualizar manualmente
- **Indicador de Conexión**: Estado de conexión al servidor

## Consulta de Estados de Cuenta

![Consulta Estados de Cuenta](/img/app-mobil/consulta-estados-cuenta.png)

Visualización detallada de movimientos y transacciones:

### Información Mostrada

#### Detalle de Movimientos

- **Fecha**: Fecha del movimiento
- **Tipo de Documento**: Factura, nota de crédito, pago, etc.
- **Número de Documento**: Folio o referencia
- **Descripción**: Detalle del movimiento
- **Importe**: Monto del cargo o abono
- **Saldo**: Balance después del movimiento

### Filtros y Búsqueda

#### Filtros Disponibles

- **Por Fecha**: Rango de fechas personalizado
- **Por Tipo de Documento**: Facturas, pagos, notas de crédito
- **Por Estado**: Pendiente, pagado, vencido
- **Por Monto**: Rango de importes
- **Por Vendedor**: Filtrar por vendedor específico

#### Búsqueda

- **Campo de Búsqueda**: Buscar por número de documento, descripción
- **Búsqueda Rápida**: Sugerencias mientras escribes
- **Filtros Combinados**: Aplicar múltiples filtros simultáneamente

### Ordenamiento

- **Por Fecha**: Ascendente o descendente
- **Por Monto**: Menor a mayor o viceversa
- **Por Documento**: Ordenar alfabéticamente
- **Por Estado**: Agrupar por estado de pago

### Acciones

- **Ver Detalle**: Expandir información del documento
- **Descargar PDF**: Obtener copia del documento
- **Compartir**: Enviar documento por email o WhatsApp
- **Seleccionar Múltiple**: Marcar varios registros

## Sumatoria de Filas Seleccionadas

![Sumatoria Filas Seleccionadas](/img/app-mobil/sumatoria-filas-seleccionadas.png)

Herramienta para análisis de registros seleccionados:

### Funcionalidad

#### Selección de Registros

- **Checkbox Individual**: Seleccionar registros específicos
- **Seleccionar Todos**: Marcar todos los registros visibles
- **Deseleccionar**: Quitar selección individual o total
- **Contador**: Número de registros seleccionados

#### Cálculos Automáticos

La aplicación calcula automáticamente:

- **Suma Total**: Total de los importes seleccionados
- **Promedio**: Promedio de montos
- **Cantidad**: Número de registros marcados

### Panel de Resultados

Ubicado en la parte inferior, muestra:

- **Total Seleccionado**: Suma de importes
- **Número de Items**: Cantidad de registros
- **Acciones Rápidas**: Exportar, compartir, limpiar selección



## Navegación y Menú

### Menú Principal

Accesible desde el ícono de hamburguesa:

- **Inicio**: Dashboard con KPIs
- **Estados de Cuenta**: Consulta detallada
- **Documentos**: Acceso a facturas y comprobantes
- **Cerrar Sesión**: Salir de forma segura

### Navegación Inferior

Barra de acceso rápido:

- **Home**: Pantalla principal
- **Consultas**: Estados de cuenta


### Limitaciones

En modo offline NO se puede:

- Actualizar datos en tiempo real
- Descargar nuevos documentos
- Enviar reportes o compartir
- Modificar configuraciones que requieren servidor


## Requisitos del Sistema

### Dispositivos Compatibles


#### Android
- Android 11.0 (Nougat) o superior
- 100 MB de espacio disponible
- Google Play Services actualizado

### Conectividad

- Conexión a Internet (WiFi o datos móviles)
- Conexión estable para sincronización en tiempo real

## Seguridad y Privacidad

### Medidas de Seguridad

- **Encriptación End-to-End**: Datos protegidos en tránsito
- **Almacenamiento Seguro**: Datos locales encriptados
- **Certificado SSL**: Comunicación segura con servidor
- **Tokens de Sesión**: Autenticación por tokens JWT

### Privacidad de Datos

- No se comparten datos con terceros
- Información financiera protegida
- Cumplimiento con regulaciones de protección de datos
- Control total sobre información personal


## Troubleshooting

### Problemas Comunes

| Problema | Solución |
|----------|----------|
| No puedo iniciar sesión | Verificar credenciales, conexión a internet |
| No veo mis empresas | Contactar administrador para verificar permisos |
| Datos desactualizados | Forzar sincronización manual |
| App lenta | Limpiar cache, reiniciar aplicación |
| No recibo notificaciones | Verificar configuración de notificaciones del dispositivo |
| Error al descargar PDF | Verificar permisos de almacenamiento |

### Restablecer Aplicación

Si persisten los problemas:

1. Cerrar sesión
2. Limpiar cache de la aplicación
3. Reiniciar dispositivo
4. Iniciar sesión nuevamente
5. Si persiste, reinstalar la aplicación

:::warning Importante
Al reinstalar la aplicación, los datos en cache se eliminarán. Asegúrate de tener conexión a internet para volver a sincronizar.
:::
