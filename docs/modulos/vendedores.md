# Vendedores

El módulo de Vendedores permite gestionar todo el catálogo de vendedores del sistema GMAS. Este módulo es fundamental para la operación comercial y ofrece funcionalidades avanzadas como importación masiva desde Excel.

## Características Principales

- **Gestión Completa**: Crear, editar y eliminar vendedores
- **Importación Masiva**: Carga de vendedores desde archivos Excel
- **Búsqueda Avanzada**: Filtros y búsqueda eficiente
- **Asignación a Usuarios**: Vinculación con usuarios del sistema
- **Gestión por Empresa**: Vendedores específicos por compañía

## Listado de Vendedores

![Lista de Vendedores](/img/vendedores/lista.png)

El listado muestra todos los vendedores registrados en el sistema:

### Información Mostrada

- **Código**: Identificador único del vendedor
- **Nombre**: Nombre completo del vendedor
- **Empresa**: Compañía a la que pertenece
- **Email**: Correo electrónico de contacto
- **Teléfono**: Número de contacto
- **Estado**: Activo/Inactivo
- **Acciones**: Editar, eliminar, ver detalles

### Funcionalidades del Listado

- **Búsqueda**: Campo de búsqueda por código, nombre o email
- **Filtros**:
  - Por empresa
  - Por estado (activo/inactivo)
  - Por zona geográfica
- **Ordenamiento**: Por cualquier columna
- **Paginación**: Navegación entre páginas
- **Exportación**: Descargar listado a Excel
- **Importación**: Botón para carga masiva

## Formulario de Vendedor

![Formulario de Vendedor](/img/vendedores/formulario.png)

### Datos Básicos

- **Código del Vendedor**: Identificador único (requerido)
- **Nombre**: Nombre completo del vendedor
- **Empresa**: Compañía a la que pertenece
- **RFC/NIT**: Identificación fiscal

### Información de Contacto

- **Email**: Correo electrónico principal
- **Email Secundario**: Correo electrónico alternativo
- **Teléfono**: Número de contacto principal
- **Teléfono Móvil**: Número celular
- **Dirección**: Domicilio completo

### Información Comercial

- **Zona**: Zona geográfica asignada
- **Territorio**: Territorio de ventas
- **Tipo de Vendedor**: Clasificación (interno, externo, distribuidor)
- **Gerente**: Supervisor o gerente asignado
- **Comisión**: Porcentaje de comisión

### Configuración

- **Estado**: Activo/Inactivo
- **Fecha de Alta**: Fecha de registro
- **Observaciones**: Notas adicionales

## Importación desde Excel

Una de las características más potentes del módulo es la capacidad de importar vendedores masivamente desde archivos Excel.

### Plantilla de Excel

![Excel Carga Masiva](/img/vendedores/excel-carga-masiva.png)

La plantilla de Excel debe contener las siguientes columnas:

- **Código**: Identificador único del vendedor
- **Nombre**: Nombre completo
- **Email**: Correo electrónico
- **Teléfono**: Número de contacto
- **Empresa**: Código o nombre de la empresa
- **RFC/NIT**: Identificación fiscal
- **Zona**: Zona asignada
- **Estado**: A (Activo) o I (Inactivo)

### Proceso de Importación

![Importación Excel](/img/vendedores/importacion-excel.png)

1. **Descargar Plantilla**: Obtener la plantilla Excel del sistema
2. **Llenar Datos**: Completar la información de los vendedores
3. **Validar Formato**: Asegurar que los datos cumplan con el formato
4. **Seleccionar Archivo**: Cargar el archivo Excel
5. **Revisar Previsualización**: Verificar los datos antes de importar
6. **Ejecutar Importación**: Confirmar la carga

### Resultado de Importación

![Resultado Importación](/img/vendedores/resultado-importacion.png)

Al finalizar la importación, el sistema muestra:

#### Resumen de Resultados

- **Total de Registros**: Número de filas procesadas
- **Exitosos**: Vendedores creados correctamente
- **Con Errores**: Registros que no pudieron ser procesados
- **Actualizados**: Vendedores existentes que fueron actualizados

#### Detalle de Errores

Para cada registro con error se muestra:

- Número de fila en el Excel
- Campo con problema
- Descripción del error
- Valor que causó el error

#### Acciones Post-Importación

- **Descargar Reporte**: Obtener detalle completo en Excel
- **Corregir Errores**: Editar el archivo y reimportar
- **Ver Registros Exitosos**: Acceder al listado de vendedores creados

## Validaciones de Importación

El sistema valida durante la importación:

### Validaciones de Formato

- Columnas requeridas presentes
- Tipos de datos correctos
- Formato de email válido
- Formato de teléfono válido

### Validaciones de Negocio

- Código de vendedor único
- Empresa existe en el sistema
- Zona válida
- Estado válido (A o I)
- RFC/NIT no duplicado

### Validaciones de Integridad

- Referencias a empresas existentes
- Referencias a zonas válidas
- Gerentes asignados existen

## Operaciones Principales

### Crear Vendedor Individual

1. Hacer clic en "Nuevo Vendedor"
2. Completar el formulario
3. Asignar empresa y zona
4. Guardar el registro

### Editar Vendedor

1. Localizar vendedor en el listado
2. Hacer clic en editar
3. Modificar los campos necesarios
4. Guardar cambios

### Importar Vendedores Masivamente

1. Hacer clic en "Importar desde Excel"
2. Descargar plantilla (si es primera vez)
3. Llenar la plantilla con los datos
4. Cargar el archivo
5. Revisar previsualización
6. Confirmar importación
7. Revisar resultados
8. Corregir errores si es necesario

### Exportar Vendedores

1. Aplicar filtros deseados (opcional)
2. Hacer clic en "Exportar a Excel"
3. Guardar el archivo generado

### Activar/Desactivar Vendedor

1. Editar el vendedor
2. Cambiar el estado
3. Guardar cambios

:::tip Mejor Práctica
Es recomendable desactivar vendedores en lugar de eliminarlos para mantener el historial de transacciones.
:::

## Consejos para Importación Excel

### Preparación del Archivo

:::info Recomendaciones
- Usar la plantilla oficial del sistema
- No modificar los nombres de las columnas
- Eliminar filas vacías
- Verificar que no haya espacios adicionales
- Usar formato de texto para códigos y RFC/NIT
:::

### Datos Requeridos

Los campos obligatorios son:
- Código
- Nombre
- Empresa
- Email

### Errores Comunes

| Error | Causa | Solución |
|-------|-------|----------|
| Código duplicado | El código ya existe | Usar código único |
| Empresa no encontrada | La empresa no existe | Verificar código de empresa |
| Email inválido | Formato incorrecto | Usar formato: usuario@dominio.com |
| Estado inválido | Valor diferente de A o I | Usar solo A o I |

## Búsqueda y Filtros

### Búsqueda Rápida

Campo de búsqueda que busca en:
- Código del vendedor
- Nombre
- Email
- Teléfono

### Filtros Avanzados

- **Por Empresa**: Filtrar vendedores de una compañía específica
- **Por Estado**: Activos, Inactivos o Todos
- **Por Zona**: Filtrar por zona geográfica
- **Por Tipo**: Filtrar por tipo de vendedor
- **Por Gerente**: Ver vendedores de un gerente específico

## Reportes

El módulo permite generar:

- **Listado General**: Todos los vendedores
- **Por Empresa**: Vendedores por compañía
- **Por Zona**: Distribución geográfica
- **Por Estado**: Activos vs Inactivos
- **Con Comisiones**: Vendedores y sus tasas de comisión

## Integración con Otros Módulos

### Usuarios

- Asignación de vendedores a usuarios
- Control de acceso por vendedor
- Notificaciones a usuarios responsables

### Compañías

- Vendedores vinculados a empresas
- Gestión multiempresa
- Reportes por compañía

### Ventas y Pedidos

- Asociación de pedidos a vendedores
- Comisiones calculadas
- Metas y objetivos

## Permisos Requeridos

Para gestionar vendedores se requiere:

- Rol de Administrador o
- Permisos de gestión de vendedores

Para importación masiva:
- Permisos adicionales de importación
- Rol de Administrador o Gerente

## Validaciones del Sistema

### Campos Únicos

- Código del vendedor
- Email principal
- RFC/NIT (por empresa)

### Campos Obligatorios

- Código
- Nombre
- Empresa
- Email
- Estado

### Reglas de Negocio

- Un vendedor debe pertenecer a al menos una empresa
- El código debe ser alfanumérico
- La comisión debe estar entre 0 y 100%
- La fecha de alta no puede ser futura

:::warning Importante
Los cambios en la información de vendedores pueden afectar cálculos de comisiones y asignación de pedidos. Asegúrese de revisar las implicaciones antes de modificar datos críticos.
:::
