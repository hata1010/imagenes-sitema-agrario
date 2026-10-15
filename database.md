## Table `documentos`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `int8` | Primary |
| `titulo` | `text` |  |
| `contenido` | `text` |  Nullable |
| `embedding` | `vector` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `fincas`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `nombre` | `text` |  |
| `representante` | `text` |  Nullable |
| `asoc_ganadera` | `text` |  Nullable |
| `pais` | `text` |  Nullable |
| `ubicacion` | `text` |  Nullable |
| `dias_gestacion` | `int4` |  Nullable |
| `formato_peso` | `text` |  Nullable |
| `formato_moneda` | `text` |  Nullable |
| `comentarios` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |
| `updated_at` | `timestamptz` |  Nullable |

## Table `config_edades_reclasificacion`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  Unique |
| `edad_becerro` | `int4` |  Nullable |
| `edad_destete` | `int4` |  Nullable |
| `edad_levante` | `int4` |  Nullable |
| `edad_vientre_ceba` | `int4` |  Nullable |
| `criterios_transicion` | `jsonb` |  Nullable |

## Table `config_categorias_animales`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  Unique |
| `nombre_becerro_m` | `text` |  Nullable |
| `nombre_becerro_h` | `text` |  Nullable |
| `nombre_destete_m` | `text` |  Nullable |
| `nombre_destete_h` | `text` |  Nullable |
| `nombre_levante_m` | `text` |  Nullable |
| `nombre_levante_h` | `text` |  Nullable |
| `nombre_ceba_m` | `text` |  Nullable |
| `nombre_vientre_h` | `text` |  Nullable |
| `nombre_toro` | `text` |  Nullable |
| `nombre_vaca` | `text` |  Nullable |

## Table `config_nomina`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  Unique |
| `conceptos` | `jsonb` |  Nullable |

## Table `sectores`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `nombre` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `potreros`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `sector_id` | `uuid` |  Nullable |
| `codigo` | `text` |  |
| `nombre` | `text` |  |
| `hectareas` | `numeric` |  Nullable |
| `carga_maxima` | `int4` |  Nullable |
| `pasto` | `text` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `lotes`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `nombre` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `grupos`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `nombre` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `razas`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `diagnosticos_veterinarios`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `tipo` | `text` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `condiciones_corporales`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `tipos_explotacion`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `calidades_animal`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `causas_muerte`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `procedencias`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `destinos_venta`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `proveedores`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `grupos_cuenta`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `animales`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `nombre` | `text` |  Nullable |
| `fecha_nacimiento` | `date` |  Nullable |
| `sexo` | `text` |  Nullable |
| `potrero_id` | `uuid` |  Nullable |
| `lote_id` | `uuid` |  Nullable |
| `grupo_id` | `uuid` |  Nullable |
| `estado` | `text` |  Nullable |
| `salud` | `text` |  Nullable |
| `seleccionado_descarte` | `bool` |  Nullable |
| `madre_id` | `uuid` |  Nullable |
| `padre_id` | `uuid` |  Nullable |
| `es_te` | `bool` |  Nullable |
| `donadora_id` | `uuid` |  Nullable |
| `tipo_servicio_padre` | `text` |  Nullable |
| `raza_id` | `uuid` |  Nullable |
| `tipo_explotacion_id` | `uuid` |  Nullable |
| `calidad_id` | `uuid` |  Nullable |
| `categoria` | `text` |  Nullable |
| `peso_nacer` | `numeric` |  Nullable |
| `tatuado` | `bool` |  Nullable |
| `herrado` | `bool` |  Nullable |
| `descornado` | `bool` |  Nullable |
| `inventariado` | `bool` |  Nullable |
| `fecha_inventario` | `date` |  Nullable |
| `id_electronica` | `text` |  Nullable |
| `fecha_compra` | `date` |  Nullable |
| `peso_compra` | `numeric` |  Nullable |
| `procedencia_id` | `uuid` |  Nullable |
| `precio_compra` | `numeric` |  Nullable |
| `nro_registro` | `text` |  Nullable |
| `asoc_ganadera` | `text` |  Nullable |
| `fecha_registro` | `date` |  Nullable |
| `clasificacion_registro` | `text` |  Nullable |
| `tipo_registro` | `text` |  Nullable |
| `comentarios_fisicos` | `jsonb` |  Nullable |
| `nro_pezones` | `int4` |  Nullable |
| `foto_url` | `text` |  Nullable |
| `hierro_url` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |
| `updated_at` | `timestamptz` |  Nullable |

## Table `tratamientos_vacunas_catalogo`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `descripcion` | `text` |  |
| `ml_mgs_dosis` | `numeric` |  Nullable |
| `tipo` | `text` |  Nullable |
| `precio_dosis` | `numeric` |  Nullable |
| `inventario` | `numeric` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `servicios_reproductivos`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `padre_id` | `uuid` |  Nullable |
| `inseminador` | `text` |  Nullable |
| `pajuela` | `text` |  Nullable |
| `dosis` | `int4` |  Nullable |
| `precio` | `numeric` |  Nullable |
| `efectivo` | `bool` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `palpaciones`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `dias_gestacion` | `int4` |  Nullable |
| `diagnostico_id` | `uuid` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `partos`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `machos` | `int4` |  Nullable |
| `hembras` | `int4` |  Nullable |
| `muertos` | `int4` |  Nullable |
| `tipo_parto` | `text` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `pesajes`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `peso` | `numeric` |  |
| `es_destete` | `bool` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `produccion_lactea`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `prod_am` | `numeric` |  Nullable |
| `prod_pm` | `numeric` |  Nullable |
| `dias_produccion` | `int4` |  Nullable |
| `secado` | `bool` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `aplicaciones_tratamiento`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `tratamiento_id` | `uuid` |  |
| `fecha` | `date` |  |
| `dosis` | `numeric` |  Nullable |
| `precio_dosis` | `numeric` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `ingresos_almacen`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `tratamiento_id` | `uuid` |  |
| `fecha` | `date` |  |
| `dosis_ingresadas` | `numeric` |  Nullable |
| `precio_dosis` | `numeric` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `revisiones_veterinarias`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `diagnostico_id` | `uuid` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `historico_reubicaciones`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `potrero_id` | `uuid` |  Nullable |
| `lote_id` | `uuid` |  Nullable |
| `grupo_id` | `uuid` |  Nullable |
| `comentario` | `text` |  Nullable |
| `hora` | `time` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `historico_comentarios`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `comentado_por` | `text` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `historico_condicion_corporal`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `animal_id` | `uuid` |  |
| `fecha` | `date` |  |
| `condicion_id` | `uuid` |  Nullable |
| `evaluado_por` | `text` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `empleados`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `codigo` | `text` |  |
| `nombres` | `text` |  |
| `apellidos` | `text` |  |
| `nro_identificacion` | `text` |  Nullable |
| `cargo` | `text` |  Nullable |
| `estado` | `text` |  Nullable |
| `fecha_ingreso` | `date` |  Nullable |
| `fecha_contrato` | `date` |  Nullable |
| `fecha_nacimiento` | `date` |  Nullable |
| `sexo` | `text` |  Nullable |
| `salario_diario` | `numeric` |  Nullable |
| `foto_url` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `pagos_nomina`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `empleado_id` | `uuid` |  |
| `fecha_pago` | `date` |  |
| `lapso_inicio` | `date` |  Nullable |
| `lapso_fin` | `date` |  Nullable |
| `dias_laborados` | `int4` |  Nullable |
| `salario_basico` | `numeric` |  Nullable |
| `asignaciones` | `jsonb` |  Nullable |
| `deducciones` | `jsonb` |  Nullable |
| `total_asignaciones` | `numeric` |  Nullable |
| `total_deducciones` | `numeric` |  Nullable |
| `total_pagar` | `numeric` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

## Table `movimientos_cuenta`

### Columns

| Name | Type | Constraints |
|------|------|-------------|
| `id` | `uuid` | Primary |
| `finca_id` | `uuid` |  |
| `grupo_cuenta_id` | `uuid` |  Nullable |
| `fecha` | `date` |  |
| `tipo` | `text` |  Nullable |
| `descripcion` | `text` |  |
| `monto` | `numeric` |  |
| `referencia` | `text` |  Nullable |
| `proveedor_id` | `uuid` |  Nullable |
| `comentario` | `text` |  Nullable |
| `created_at` | `timestamptz` |  Nullable |

