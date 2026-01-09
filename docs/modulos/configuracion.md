# Configuración de la Aplicación

El módulo de Configuración de la Aplicación es una sección administrativa que permite configurar los parámetros esenciales del sistema GMAS. Aquí se gestionan las integraciones y configuraciones técnicas necesarias para el funcionamiento del sistema.

## Características Principales

- **Integración con Business Central**: Conexión con Microsoft Dynamics 365 Business Central
- **Gestión de Sesiones JWT**: Configuración de autenticación y tokens
- **Configuración SMTP**: Servidor de correo electrónico para notificaciones
- **Parámetros del Sistema**: Configuraciones generales de la aplicación

## Integración con Business Central

![Configuración Business Central](/img/aplicacion/business-central.png)

La integración con Microsoft Dynamics 365 Business Central permite sincronizar datos entre GMAS y el ERP empresarial.

### Configuración de Conexión

#### Datos de Conexión

- **URL del Servidor**: Dirección del servidor Business Central
- **Empresa**: Nombre de la empresa en Business Central
- **Puerto**: Puerto de conexión (generalmente 7048 para HTTP o 7049 para HTTPS)
- **Protocolo**: HTTP o HTTPS

#### Autenticación

- **Tipo de Autenticación**:
  - Windows Authentication
  - OAuth 2.0
  - Basic Authentication
- **Usuario**: Cuenta de servicio para la conexión
- **Contraseña**: Credencial de acceso
- **Token de Acceso**: Para autenticación OAuth (si aplica)

#### Configuración Avanzada

- **Timeout de Conexión**: Tiempo máximo de espera (en segundos)
- **Reintentos**: Número de intentos en caso de fallo
- **Ambiente**: Producción, Desarrollo, Pruebas
- **API Version**: Versión de la API de Business Central

### Sincronización de Datos

#### Entidades Sincronizables

- **Clientes**: Sincronización de catálogo de clientes
- **Vendedores**: Actualización de vendedores desde BC
- **Productos**: Catálogo de productos y servicios
- **Pedidos**: Envío de pedidos a Business Central
- **Inventario**: Consulta de existencias
- **Precios**: Actualización de listas de precios

#### Configuración de Sincronización

- **Modo de Sincronización**:
  - Manual
  - Automática (programada)
  - Tiempo real (webhook)
- **Frecuencia**: Cada X minutos/horas
- **Horario**: Definir ventanas de sincronización
- **Dirección**:
  - Unidireccional (BC → GMAS)
  - Bidireccional (BC ↔ GMAS)

### Prueba de Conexión

1. Configurar los parámetros de conexión
2. Hacer clic en "Probar Conexión"
3. Verificar el resultado:
   - ✅ Conexión exitosa
   - ❌ Error de conexión (revisar logs)
4. Guardar configuración si la prueba es exitosa

### Logs de Integración

El sistema registra:

- Intentos de conexión
- Sincronizaciones exitosas
- Errores y excepciones
- Datos transferidos
- Tiempo de respuesta

:::warning Importante
Las credenciales de Business Central deben tener los permisos necesarios para leer y escribir en las entidades configuradas.
:::

## Gestión de Sesiones JWT

![Configuración JWT y Sesiones](/img/aplicacion/jwt-sesiones.png)

JSON Web Tokens (JWT) se utilizan para la autenticación y gestión de sesiones de usuario en GMAS.

### Configuración de JWT

#### Parámetros de Token

- **Secret Key**: Clave secreta para firmar tokens (debe ser compleja y segura)
- **Algoritmo**: Algoritmo de encriptación (HS256, HS512, RS256)
- **Issuer**: Emisor del token (identificador del sistema)
- **Audience**: Audiencia del token (destinatario válido)

#### Tiempo de Vida

- **Tiempo de Expiración**: Duración de validez del token
  - Tokens de acceso: 15-30 minutos (recomendado)
  - Tokens de actualización: 7-30 días
- **Renovación Automática**: Activar/desactivar renovación
- **Ventana de Renovación**: Tiempo antes de expiración para permitir renovación

#### Configuración de Seguridad

- **Incluir Claims Personalizados**: Información adicional en el token
  - ID de usuario
  - Rol
  - Empresas asignadas
  - Permisos específicos
- **Validar IP**: Verificar que el token se use desde la misma IP
- **Validar User Agent**: Verificar navegador/dispositivo
- **Token Único por Dispositivo**: Permitir/bloquear múltiples sesiones

### Gestión de Sesiones

#### Configuración de Sesiones

- **Sesiones Concurrentes**: Número máximo de sesiones simultáneas por usuario
  - 1: Solo una sesión activa
  - Ilimitado: Múltiples dispositivos permitidos
- **Tiempo de Inactividad**: Minutos de inactividad antes de cerrar sesión (30 min recomendado)
- **Persistencia de Sesión**: Mantener sesión al cerrar navegador

#### Control de Sesiones Activas

- **Visualizar Sesiones**: Ver todas las sesiones activas del usuario
- **Cerrar Sesión Remota**: Terminar sesiones específicas
- **Cerrar Todas las Sesiones**: Forzar cierre de todas las sesiones (útil en caso de seguridad)

#### Registro de Sesiones

El sistema registra:

- Fecha y hora de inicio de sesión
- Dirección IP
- Dispositivo/Navegador
- Ubicación geográfica (si está disponible)
- Duración de la sesión
- Fecha y hora de cierre

### Seguridad JWT

:::tip Mejores Prácticas
- Usar claves secretas complejas (mínimo 256 bits)
- Cambiar la clave secreta periódicamente
- No almacenar información sensible en el payload del JWT
- Implementar lista negra de tokens revocados
- Usar HTTPS siempre para transmitir tokens
- Almacenar tokens en lugares seguros (no en localStorage para datos sensibles)
:::

### Revocación de Tokens

- **Revocación Manual**: Invalidar tokens específicos
- **Revocación Automática**: Por cambio de contraseña o permisos
- **Lista Negra**: Mantener registro de tokens revocados

## Configuración SMTP

![Configuración SMTP](/img/aplicacion/smpt.png)

La configuración del servidor SMTP permite al sistema enviar correos electrónicos para notificaciones, alertas y comunicaciones.

### Datos del Servidor SMTP

#### Información de Conexión

- **Servidor SMTP**: Dirección del servidor de correo
  - Gmail: smtp.gmail.com
  - Outlook: smtp.office365.com
  - Personalizado: tu-servidor-smtp.com
- **Puerto**: Puerto de conexión
  - 25: Sin encriptación (no recomendado)
  - 587: TLS/STARTTLS (recomendado)
  - 465: SSL
- **Seguridad**: Tipo de encriptación
  - Ninguna
  - TLS/STARTTLS
  - SSL

#### Autenticación

- **Requiere Autenticación**: Sí/No
- **Usuario**: Cuenta de correo para envío
- **Contraseña**: Contraseña o contraseña de aplicación
- **Nombre del Remitente**: Nombre que aparecerá en los correos
- **Email del Remitente**: Dirección de correo del remitente

### Configuración Avanzada

#### Parámetros de Envío

- **Timeout**: Tiempo máximo de espera (segundos)
- **Reintentos**: Intentos en caso de fallo
- **Límite de Envíos**: Correos por hora/día (para evitar bloqueos)
- **Pool de Conexiones**: Número de conexiones simultáneas

#### Plantillas de Correo

- **Usar Plantillas HTML**: Activar diseño personalizado
- **Pie de Firma**: Firma automática en correos
- **Encabezado**: Logo o encabezado corporativo
- **Codificación**: UTF-8 (recomendado para caracteres especiales)

### Tipos de Correos del Sistema

El sistema puede enviar:

#### Correos de Autenticación
- Bienvenida a nuevo usuario
- Recuperación de contraseña
- Confirmación de cambio de contraseña
- Notificación de sesión sospechosa

#### Correos Operativos
- Asignación de empresas o vendedores
- Cambios en permisos
- Notificaciones de pedidos
- Alertas de inventario
- Reportes programados

#### Correos Administrativos
- Errores del sistema
- Notificaciones de sincronización
- Alertas de seguridad
- Resúmenes diarios/semanales

### Prueba de Configuración SMTP

1. Configurar los parámetros del servidor
2. Ingresar credenciales
3. Hacer clic en "Enviar Correo de Prueba"
4. Ingresar email de destino
5. Verificar recepción del correo
6. Guardar configuración si la prueba es exitosa

### Proveedores SMTP Comunes

#### Gmail

```
Servidor: smtp.gmail.com
Puerto: 587
Seguridad: TLS
Nota: Requiere "Contraseña de aplicación" si tienes 2FA activado
```

#### Microsoft 365 / Outlook

```
Servidor: smtp.office365.com
Puerto: 587
Seguridad: TLS
Autenticación: OAuth 2.0 o Basic
```

#### SendGrid

```
Servidor: smtp.sendgrid.net
Puerto: 587
Usuario: apikey
Contraseña: Tu API Key de SendGrid
```

### Troubleshooting SMTP

| Problema | Posible Causa | Solución |
|----------|---------------|----------|
| No se pueden enviar correos | Credenciales incorrectas | Verificar usuario y contraseña |
| Timeout de conexión | Firewall bloqueando | Verificar reglas de firewall |
| Correos en spam | Falta autenticación SPF/DKIM | Configurar registros DNS |
| Error 535 | Autenticación fallida | Usar contraseña de aplicación |
| Puerto bloqueado | ISP bloquea puerto 25 | Usar puerto 587 o 465 |

:::warning Seguridad
- No usar cuentas personales para envío masivo
- Crear cuenta de servicio dedicada
- Usar contraseñas de aplicación cuando sea posible
- Habilitar 2FA en la cuenta de correo
- Monitorear logs de envío para detectar abuso
:::

## Parámetros Generales del Sistema

### Configuración Regional

- **Idioma por Defecto**: Idioma de la interfaz
- **Zona Horaria**: Configuración de horario del servidor
- **Formato de Fecha**: DD/MM/YYYY, MM/DD/YYYY, etc.
- **Formato de Moneda**: Símbolo y formato
- **Separador Decimal**: Punto o coma

### Configuración de la Aplicación

- **Nombre de la Aplicación**: Título mostrado
- **Logo**: Logo corporativo
- **Favicon**: Icono del navegador
- **Modo de Mantenimiento**: Activar/desactivar acceso
- **Mensaje de Mantenimiento**: Texto a mostrar durante mantenimiento

### Límites y Restricciones

- **Máximo de Registros por Página**: Paginación
- **Tamaño Máximo de Archivo**: Para importaciones
- **Tiempo de Sesión**: Minutos de inactividad permitidos
- **Intentos de Login**: Antes de bloquear cuenta

## Respaldo y Restauración

### Configuración de Respaldos

- **Respaldos Automáticos**: Activar/desactivar
- **Frecuencia**: Diaria, semanal, mensual
- **Horario**: Hora de ejecución
- **Retención**: Días de conservación de respaldos
- **Ubicación**: Ruta de almacenamiento

### Restauración

- Seleccionar punto de restauración
- Confirmar restauración
- Verificar integridad de datos

## Logs y Auditoría

### Configuración de Logs

- **Nivel de Log**: Debug, Info, Warning, Error
- **Retención de Logs**: Días de conservación
- **Rotación de Logs**: Tamaño máximo por archivo
- **Destino**: Archivo, Base de datos, Servicio externo

### Auditoría

Registro de:
- Cambios en configuración
- Acciones administrativas
- Modificaciones de datos críticos
- Accesos y permisos

## Permisos Requeridos

Para acceder a la configuración de la aplicación:

- Rol de Administrador del Sistema
- Permisos específicos de configuración

:::danger Precaución
Los cambios en la configuración de la aplicación pueden afectar el funcionamiento de todo el sistema. Asegúrese de entender las implicaciones antes de modificar parámetros críticos.
:::

## Respaldo de Configuración

Antes de realizar cambios importantes:

1. Exportar configuración actual
2. Documentar cambios a realizar
3. Realizar cambios en ambiente de prueba (si está disponible)
4. Aplicar cambios en producción
5. Verificar funcionamiento
6. Mantener respaldo por si se requiere revertir

:::tip Recomendación
Documentar todos los cambios en configuración con fecha, responsable y razón del cambio.
:::
