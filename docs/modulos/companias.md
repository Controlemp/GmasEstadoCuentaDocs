# Compañías

El módulo de Compañías permite gestionar las empresas que forman parte del sistema GMAS. Este módulo es fundamental para la configuración multiempresa del sistema.

## Características Principales

- **Gestión Completa**: Crear, editar y eliminar compañías
- **Listado Organizado**: Visualización clara de todas las compañías registradas
- **Búsqueda y Filtros**: Herramientas para localizar compañías rápidamente

## Listado de Compañías

![Listado de Compañías](/img/companias/listado.png)

El listado muestra:

- Nombre de la compañía
- Información de contacto
- Estado de la compañía
- Acciones disponibles (editar, eliminar)

### Funcionalidades del Listado

- **Búsqueda**: Campo de búsqueda para filtrar compañías
- **Ordenamiento**: Ordenar por diferentes columnas
- **Paginación**: Navegación entre páginas de resultados
- **Acciones Rápidas**: Botones para editar o eliminar registros

## Formulario de Compañía

![Formulario de Compañía](/img/companias/formulario.png)

El formulario permite capturar toda la información necesaria de la compañía:

### Datos Básicos

- **Nombre de la Compañía**: Denominación oficial
- **Razón Social**: Nombre legal de la empresa
- **RFC/NIT**: Identificación fiscal
- **Código**: Identificador interno de la compañía

### Información de Contacto

- **Dirección**: Domicilio fiscal y operativo
- **Teléfono**: Número de contacto principal
- **Email**: Correo electrónico de contacto
- **Sitio Web**: URL del sitio web corporativo

### Configuración

- **Estado**: Activo/Inactivo
- **Configuraciones Específicas**: Parámetros particulares de la compañía

## Operaciones Disponibles

### Crear Nueva Compañía

1. Hacer clic en el botón "Nueva Compañía"
2. Completar el formulario con los datos requeridos
3. Guardar los cambios

### Editar Compañía

1. Localizar la compañía en el listado
2. Hacer clic en el botón de editar
3. Modificar los campos necesarios
4. Guardar los cambios

### Eliminar Compañía

1. Localizar la compañía en el listado
2. Hacer clic en el botón de eliminar
3. Confirmar la eliminación

:::warning Eliminación de Compañías
Al eliminar una compañía, se debe verificar que no tenga datos asociados (usuarios, vendedores, etc.) que puedan verse afectados.
:::

## Validaciones

El sistema valida:

- **Campos Obligatorios**: Nombre, RFC/NIT son requeridos
- **Formato de Email**: Validación de correos electrónicos
- **RFC/NIT Único**: No se permiten identificadores fiscales duplicados

## Permisos Requeridos

Para acceder a este módulo se requiere:

- Rol de Administrador o
- Permisos específicos de gestión de compañías

:::tip Mejores Prácticas
- Mantener actualizada la información de contacto
- Usar códigos descriptivos y únicos
- Verificar la información fiscal antes de guardar
- Revisar periódicamente las compañías inactivas
:::
