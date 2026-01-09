# Perfil de Usuario

El módulo de Perfil permite a cada usuario gestionar su propia información personal y configuración de cuenta. Es una sección de autogestión donde los usuarios pueden actualizar sus datos y mantener la seguridad de su cuenta.

## Características Principales

- **Gestión de Datos Personales**: Actualizar información de perfil
- **Cambio de Contraseña**: Modificar credenciales de acceso
- **Configuración de Cuenta**: Preferencias personales
- **Visualización de Permisos**: Ver roles y accesos asignados

## Información Personal

![Información Personal](/img/perfil/informacion-personal.png)

La sección de información personal permite visualizar y editar:

### Datos Personales

- **Nombre**: Nombre(s) del usuario
- **Apellidos**: Apellidos completos
- **Email**: Correo electrónico (usado para login y notificaciones)
- **Teléfono**: Número de contacto
- **Puesto**: Cargo o posición

### Información de Cuenta

- **Usuario**: Nombre de usuario para acceso
- **Rol**: Nivel de permisos asignado (solo visualización)
- **Estado**: Estado de la cuenta (solo visualización)
- **Empresas Asignadas**: Compañías a las que tiene acceso
- **Fecha de Registro**: Fecha de creación de la cuenta

### Preferencias

- **Idioma**: Idioma de la interfaz
- **Zona Horaria**: Configuración de horario
- **Notificaciones por Email**: Activar/desactivar notificaciones

## Editar Información Personal

### Campos Editables

Los usuarios pueden modificar:

- Nombre y apellidos
- Teléfono de contacto
- Preferencias de notificación
- Configuración regional

### Campos No Editables

Los siguientes campos solo pueden ser modificados por un administrador:

- Email (usado como identificador)
- Nombre de usuario
- Rol y permisos
- Estado de la cuenta
- Empresas asignadas

### Proceso de Actualización

1. Acceder a "Mi Perfil" desde el menú de usuario
2. Hacer clic en "Editar Información"
3. Modificar los campos deseados
4. Guardar los cambios
5. Confirmar actualización

:::info Validación
Los cambios en información personal requieren confirmación y pueden estar sujetos a validación administrativa según las políticas de la empresa.
:::

## Cambio de Contraseña

![Cambio de Contraseña](/img/perfil/cambio-contraseña.png)

La funcionalidad de cambio de contraseña permite a los usuarios actualizar sus credenciales de forma segura.

### Formulario de Cambio de Contraseña

El formulario requiere:

1. **Contraseña Actual**: Para verificar identidad
2. **Nueva Contraseña**: La nueva contraseña deseada
3. **Confirmar Nueva Contraseña**: Confirmación de la nueva contraseña

### Requisitos de Contraseña

Las contraseñas deben cumplir con las siguientes políticas de seguridad:

#### Requisitos Mínimos

- **Longitud**: Mínimo 8 caracteres
- **Letras Mayúsculas**: Al menos 1 letra mayúscula
- **Letras Minúsculas**: Al menos 1 letra minúscula
- **Números**: Al menos 1 dígito numérico
- **Caracteres Especiales**: Al menos 1 carácter especial (@, #, $, %, etc.)

#### Restricciones

- No puede ser igual a contraseñas anteriores (últimas 5)
- No debe contener información personal obvia (nombre, fecha de nacimiento)
- No usar secuencias comunes (123456, abcdef)
- No usar palabras del diccionario

### Proceso de Cambio

1. Acceder a "Mi Perfil"
2. Seleccionar "Cambiar Contraseña"
3. Ingresar contraseña actual
4. Ingresar nueva contraseña
5. Confirmar nueva contraseña
6. Hacer clic en "Cambiar Contraseña"
7. Recibir confirmación por email

### Indicador de Fortaleza

El sistema muestra en tiempo real la fortaleza de la contraseña:

- 🔴 **Débil**: No cumple requisitos mínimos
- 🟡 **Media**: Cumple requisitos básicos
- 🟢 **Fuerte**: Cumple todos los requisitos
- 🟢 **Muy Fuerte**: Excede requisitos con caracteres adicionales

### Mensajes de Error Comunes

| Error | Causa | Solución |
|-------|-------|----------|
| Contraseña actual incorrecta | La contraseña ingresada no coincide | Verificar contraseña actual |
| Las contraseñas no coinciden | Nueva contraseña y confirmación diferentes | Asegurar que ambas sean iguales |
| Contraseña muy corta | Menos de 8 caracteres | Usar al menos 8 caracteres |
| Falta carácter especial | No incluye símbolos | Agregar @, #, $, %, etc. |
| Contraseña ya usada | Se usó recientemente | Elegir una contraseña diferente |

## Seguridad de la Cuenta

### Buenas Prácticas

:::tip Recomendaciones de Seguridad
- Cambiar la contraseña periódicamente (cada 90 días)
- No compartir credenciales con nadie
- Usar contraseñas únicas (no reutilizar)
- No guardar contraseñas en navegadores compartidos
- Cerrar sesión al terminar de usar el sistema
- Reportar cualquier actividad sospechosa
:::

### Recuperación de Contraseña

Si olvidas tu contraseña:

1. Hacer clic en "¿Olvidaste tu contraseña?" en la pantalla de login
2. Ingresar tu email registrado
3. Revisar correo electrónico
4. Hacer clic en el enlace de recuperación
5. Establecer nueva contraseña
6. Iniciar sesión con la nueva contraseña

:::warning Tiempo de Expiración
Los enlaces de recuperación expiran después de 24 horas por seguridad.
:::

### Bloqueo de Cuenta

La cuenta se bloquea automáticamente después de:

- 5 intentos fallidos de login consecutivos
- Inactividad prolongada (según políticas de la empresa)
- Detección de actividad sospechosa

Para desbloquear una cuenta bloqueada:
- Contactar al administrador del sistema
- Verificar identidad
- Restablecer contraseña

## Configuración de Notificaciones

### Tipos de Notificaciones

Los usuarios pueden configurar preferencias para:

- **Notificaciones de Sistema**: Actualizaciones y mantenimiento
- **Notificaciones de Cuenta**: Cambios en perfil y seguridad
- **Notificaciones Operativas**: Actividades relacionadas con el trabajo
- **Recordatorios**: Tareas pendientes y vencimientos

### Canales de Notificación

- Email
- Notificaciones en la aplicación
- SMS (si está configurado)

## Visualización de Permisos

En el perfil, los usuarios pueden ver:

- **Rol Asignado**: Nivel de acceso general
- **Módulos Accesibles**: Secciones del sistema disponibles
- **Empresas Asignadas**: Compañías a las que tienen acceso
- **Vendedores Asignados**: Vendedores que pueden gestionar
- **Permisos Específicos**: Capacidades detalladas por módulo

:::info Solo Lectura
La información de permisos es solo de consulta. Para modificaciones, contactar al administrador.
:::

## Historial de Actividad

El perfil puede incluir:

- Último inicio de sesión
- Cambios recientes en la cuenta
- Historial de cambios de contraseña
- Dispositivos desde donde se ha accedido

## Cierre de Sesión

### Cerrar Sesión Manual

1. Hacer clic en el nombre de usuario (esquina superior derecha)
2. Seleccionar "Cerrar Sesión"
3. Confirmación de cierre exitoso

### Cierre Automático

El sistema cierra la sesión automáticamente:

- Después de 30 minutos de inactividad
- Al cerrar el navegador (según configuración)
- Por razones de seguridad (actualización de permisos)

## Privacidad y Datos Personales

### Protección de Datos

- Los datos personales están protegidos según normativas vigentes
- Solo administradores autorizados pueden ver información sensible
- Los cambios quedan registrados en auditoría
- Los datos no se comparten con terceros sin autorización

### Solicitudes sobre Datos Personales

Los usuarios pueden solicitar:

- Copia de sus datos personales
- Corrección de información incorrecta
- Eliminación de datos (sujeto a políticas)

## Soporte

Para ayuda con el perfil:

- **Problemas de acceso**: Contactar a soporte técnico
- **Cambios en permisos**: Contactar al administrador
- **Dudas generales**: Consultar documentación o soporte

:::tip Contacto
Para asistencia inmediata, contactar al administrador del sistema o al departamento de TI.
:::
