# Usuarios

El módulo de Usuarios es el centro de administración para la gestión de cuentas de usuario del sistema GMAS. Permite crear, modificar y administrar usuarios con diferentes niveles de acceso.

## Características Principales

- **Gestión Completa de Usuarios**: Crear, editar y eliminar cuentas
- **Asignación de Empresas**: Vincular usuarios a compañías específicas
- **Asignación de Vendedores**: Relacionar usuarios con vendedores
- **Control de Accesos**: Gestión de permisos y roles
- **Seguridad**: Cambio de contraseñas y gestión de credenciales

## Listado de Usuarios

![Listado de Usuarios](/img/usuarios/listado.png)

El listado proporciona una vista completa de todos los usuarios del sistema:

- **Nombre y Apellidos**: Identificación del usuario
- **Email**: Correo electrónico de acceso
- **Rol**: Nivel de permisos asignado
- **Estado**: Activo/Inactivo
- **Acciones**: Editar, eliminar, gestionar asignaciones

### Funcionalidades del Listado

- **Búsqueda Avanzada**: Filtrar por nombre, email o rol
- **Ordenamiento**: Organizar por diferentes criterios
- **Paginación**: Navegación eficiente entre registros
- **Acciones Rápidas**: Acceso directo a funciones de edición

## Crear Nuevo Usuario

![Crear Nuevo Usuario](/img/usuarios/crear-nuevo-usuario.png)

### Información Personal

El formulario de creación incluye:

- **Nombre**: Nombre(s) del usuario
- **Apellidos**: Apellidos del usuario
- **Email**: Correo electrónico (usado para iniciar sesión)
- **Teléfono**: Número de contacto
- **Puesto**: Cargo o posición en la empresa

### Datos de Acceso

- **Usuario**: Nombre de usuario para el login
- **Contraseña**: Contraseña inicial (debe ser cambiada en el primer acceso)
- **Confirmar Contraseña**: Verificación de la contraseña
- **Rol**: Asignación de nivel de permisos

### Configuración Adicional

- **Estado**: Activar/Desactivar cuenta
- **Forzar Cambio de Contraseña**: Obligar cambio en primer acceso

## Información Personal del Usuario

![Información Personal](/img/usuarios/informacion-personal.png)

Vista detallada del perfil del usuario que muestra:

- Datos personales completos
- Información de contacto
- Rol y permisos asignados
- Empresas asociadas
- Vendedores vinculados
- Historial de cambios

### Edición de Información Personal

Permite actualizar:

- Nombre y apellidos
- Información de contacto
- Datos del puesto
- Configuración de notificaciones

## Gestión de Contraseñas

![Cambiar Contraseña](/img/usuarios/cambiar-contraseña.png)

### Cambio de Contraseña por Administrador

El administrador puede:

- Establecer nueva contraseña
- Forzar cambio en siguiente acceso
- Desbloquear cuenta
- Resetear credenciales

### Requisitos de Contraseña

Las contraseñas deben cumplir:

- Mínimo 8 caracteres
- Al menos una letra mayúscula
- Al menos una letra minúscula
- Al menos un número
- Al menos un carácter especial

## Empresas Asignadas

![Empresas Asignadas](/img/usuarios/empresas-asignadas.png)

Gestión de las compañías a las que el usuario tiene acceso:

### Funcionalidades

- **Asignar Empresas**: Vincular usuario a una o más compañías
- **Remover Asignaciones**: Quitar acceso a compañías específicas
- **Visualizar Permisos**: Ver nivel de acceso por empresa
- **Empresa Principal**: Definir empresa por defecto

### Proceso de Asignación

1. Seleccionar usuario
2. Hacer clic en "Empresas Asignadas"
3. Seleccionar las empresas del listado
4. Definir permisos específicos por empresa
5. Guardar cambios

## Vendedores Asignados

![Vendedores Asignados](/img/usuarios/vendedores-asignados.png)

Vinculación de usuarios con vendedores del sistema:

### Características

- **Asignación Múltiple**: Un usuario puede gestionar varios vendedores
- **Visualización Clara**: Listado de vendedores asociados
- **Gestión Rápida**: Agregar o remover asignaciones
- **Filtrado**: Buscar vendedores disponibles

### Casos de Uso

- Gerentes que supervisan múltiples vendedores
- Usuarios de soporte que atienden a vendedores específicos
- Administradores que requieren acceso a información de vendedores

## Operaciones Principales

### Crear Usuario

1. Hacer clic en "Nuevo Usuario"
2. Completar información personal
3. Establecer credenciales de acceso
4. Asignar rol y permisos
5. Guardar el usuario

### Editar Usuario

1. Localizar usuario en el listado
2. Hacer clic en editar
3. Modificar los campos necesarios
4. Actualizar asignaciones si es necesario
5. Guardar cambios

### Desactivar Usuario

1. Acceder a la edición del usuario
2. Cambiar estado a "Inactivo"
3. Guardar cambios

:::warning Importante
Los usuarios inactivos no pueden iniciar sesión pero sus datos se mantienen en el sistema.
:::

### Eliminar Usuario

1. Verificar que el usuario no tenga datos críticos asociados
2. Hacer clic en eliminar
3. Confirmar la eliminación

:::danger Precaución
La eliminación de usuarios es permanente. Se recomienda desactivar en lugar de eliminar.
:::

## Roles y Permisos

### Tipos de Roles

- **Administrador**: Acceso total al sistema
- **Gerente**: Gestión de usuarios y operaciones
- **Supervisor**: Supervisión de vendedores y reportes
- **Usuario**: Acceso limitado a funciones específicas
- **Consulta**: Solo lectura de información

### Gestión de Permisos

Los permisos se asignan por:

- Módulos del sistema
- Operaciones (crear, leer, actualizar, eliminar)
- Empresas específicas
- Áreas funcionales

## Validaciones del Sistema

El sistema valida:

- **Email Único**: No se permiten correos duplicados
- **Usuario Único**: Nombres de usuario únicos
- **Campos Obligatorios**: Nombre, email, usuario son requeridos
- **Formato de Email**: Validación de correos electrónicos
- **Fortaleza de Contraseña**: Cumplimiento de políticas de seguridad

## Seguridad

### Medidas de Seguridad

- Encriptación de contraseñas
- Sesiones con tiempo de expiración
- Registro de actividad de usuarios
- Bloqueo por intentos fallidos
- Autenticación de dos factores (opcional)

### Buenas Prácticas

:::tip Recomendaciones
- Revisar periódicamente usuarios activos
- Desactivar cuentas de empleados que ya no laboran
- Asignar el menor nivel de permisos necesario
- Forzar cambio de contraseña periódicamente
- Auditar accesos y actividades regularmente
:::

## Permisos Requeridos

Para gestionar usuarios se requiere:

- Rol de Administrador o
- Permisos específicos de gestión de usuarios

## Notificaciones

El sistema envía notificaciones automáticas para:

- Creación de nueva cuenta
- Cambio de contraseña
- Modificación de permisos
- Asignación de empresas o vendedores
- Activación/Desactivación de cuenta
