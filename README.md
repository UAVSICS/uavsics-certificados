# uavsics-certificados
Sistema de validación pública de certificados UAVSICS
# Sistema de Certificación UAVSICS

## Información General

**Nombre del Proyecto:** Sistema de Certificación UAVSICS
**Organización:** UAVSICS
**Sitio de Validación:** https://uavsics.github.io/uavsics-certificados/
**Correo de Soporte:** [soporte@uavsics.cl](mailto:soporte@uavsics.cl)

### Objetivo

El Sistema de Certificación UAVSICS permite emitir, registrar, validar y, cuando corresponda, revocar certificados de capacitación emitidos por UAVSICS.

Cada certificado cuenta con:

* Código único de identificación.
* Certificado PDF individual.
* Código QR de validación.
* Registro en base de datos maestra.
* Validación pública en línea.
* Estado de vigencia (Válido o Revocado).

---

# Arquitectura General

El sistema se compone de cuatro elementos principales:

## 1. Base de Datos Maestra

Archivo:

UAVSICS_Certificados_Maestro

Función:

* Almacenar todos los certificados emitidos.
* Gestionar el estado de cada certificado.
* Proveer la información utilizada para la validación pública.

---

## 2. Generador de Certificados

Permite:

* Ingresar los datos del alumno.
* Seleccionar el curso.
* Registrar horas cronológicas.
* Registrar fechas de inicio y término.
* Generar automáticamente el certificado PDF.

---

## 3. Sistema de Validación Pública

Sitio web:

https://uavsics.github.io/uavsics-certificados/

Permite:

* Consultar certificados mediante código único.
* Consultar certificados mediante código QR.
* Verificar vigencia.
* Acceder al certificado PDF asociado.

---

## 4. Archivo JSON

Archivo:

certificados.json

Función:

* Publicar los registros necesarios para la validación.
* Actualizar automáticamente la información visible en el portal de validación.

---

# Estructura de Carpetas

UAVSICS/

├── 01_Certificaciones

│ ├── 01_Base_de_Datos

│ │ └── UAVSICS_Certificados_Maestro

│ ├── 02_Certificados_Emitidos

│ ├── 03_Plantillas

│ │ └── 02_Plantilla_Certificado_UAVSICS

│ ├── 04_QR

│ ├── 05_Manuales

│ └── 06_Firmas

│ ├── Firma_Eduardo_Perez.png

│ └── Firma_Jorge_Poblete.png

---

# Flujo de Emisión de Certificados

## Paso 1

Ingresar:

* Nombre del alumno.
* Curso.
* Horas cronológicas.
* Fecha de inicio.
* Fecha de término.

## Paso 2

Presionar:

"Generar Certificado"

## Paso 3

El sistema ejecuta automáticamente:

* Generación del PDF.
* Asignación de código único.
* Registro en la base de datos.
* Actualización de certificados.json.
* Inserción de código QR.
* Almacenamiento del certificado emitido.

## Paso 4

El certificado generado se almacena en:

02_Certificados_Emitidos

## Paso 5

El certificado es firmado electrónicamente por el responsable autorizado.

---

# Validación de Certificados

Los certificados pueden verificarse mediante:

### Código de Certificado

Ejemplo:

UAVSICS-2026-0001

### Código QR

El QR dirige automáticamente al sistema de validación.

---

# Estados de Certificación

## Válido

Indica que el certificado se encuentra vigente y reconocido por UAVSICS.

## Revocado

Indica que el certificado ha sido invalidado y no debe considerarse vigente.

---

# Control de Accesos

Administradores autorizados:

* Jorge Poblete
* Eduardo Pérez

Cuenta operativa:

* [soporte@uavsics.cl](mailto:soporte@uavsics.cl)

Se recomienda restringir el acceso únicamente a personal autorizado.

---

# Firma Electrónica

Los certificados incorporan firmas institucionales en la plantilla de emisión.

Posteriormente, el certificado PDF puede ser firmado electrónicamente mediante firma electrónica simple para reforzar su autenticidad y trazabilidad.

---

# Respaldo del Sistema

Se recomienda mantener respaldo periódico de:

* UAVSICS_Certificados_Maestro.
* Certificados PDF emitidos.
* Repositorio GitHub.
* Plantillas de certificados.
* Archivos de firmas institucionales.

Frecuencia recomendada:

* Respaldo mensual.
* Respaldo extraordinario antes de modificaciones relevantes.

---

# Recuperación ante Incidentes

En caso de pérdida de información:

1. Restaurar la base de datos maestra.
2. Restaurar los certificados emitidos.
3. Restaurar el repositorio GitHub.
4. Verificar la publicación de certificados.json.
5. Validar la operación del portal público.

---

# Control de Versiones

| Versión | Fecha      | Responsable   | Descripción                            |
| ------- | ---------- | ------------- | -------------------------------------- |
| 1.0     | Julio 2026 | Jorge Poblete | Implementación inicial del sistema     |
| 1.1     | Pendiente  | UAVSICS       | Incorporación de dominio personalizado |
| 1.2     | Pendiente  | UAVSICS       | Mejoras futuras y mantenimiento        |

---

© UAVSICS - Sistema de Certificación UAVSICS
