# 1. Tipos de Datos

Los datos son la materia prima del análisis de datos, la inteligencia de negocios (BI) y la ciencia de datos. Dependiendo de su estructura y organización, se clasifican en tres categorías principales: estructurados, semiestructurados y no estructurados.


# A. Datos Estructurados

Los datos estructurados son aquellos que se encuentran organizados en filas y columnas siguiendo un formato definido. Son fáciles de almacenar, consultar y analizar mediante bases de datos relacionales.

## Características

- Tienen una estructura fija y predefinida.
- Se almacenan en tablas.
- Son fáciles de consultar mediante SQL.
- Facilitan la generación de reportes y análisis.
- Son ampliamente utilizados en sistemas empresariales.

## Ejemplos

- Bases de datos SQL (MySQL, SQL Server, PostgreSQL).
- Archivos de Excel.
- Sistemas ERP y CRM.
- Reportes de Power BI.
- Inventarios de productos.

## Ejemplo de Tabla

| ID | Nombre | Edad | Ciudad |
|----|---------|------|---------|
| 1 | Juan | 25 | Bogotá |
| 2 | María | 30 | Medellín |
| 3 | Carlos | 28 | Cali |

## Caso de Uso

Una empresa almacena la información de sus clientes en una base de datos SQL para generar reportes de ventas y analizar tendencias de compra.





# B. Datos Semiestructurados

Los datos semiestructurados poseen cierto nivel de organización, pero no siguen una estructura rígida como las tablas de una base de datos relacional.

## Características

- No requieren un esquema fijo.
- Utilizan etiquetas, claves o atributos para organizar la información.
- Son más flexibles que los datos estructurados.
- Pueden variar entre registros sin afectar el almacenamiento.
- Son comunes en aplicaciones web y APIs.

## Ejemplos

- JSON
- XML
- Archivos YAML
- Correos electrónicos
- Respuestas de APIs

## Ejemplo en JSON

```json
{
  "nombre": "Juan",
  "edad": 25,
  "ciudad": "Bogotá"
}
```

## Ejemplo en XML

```xml
<persona>
    <nombre>Juan</nombre>
    <edad>25</edad>
    <ciudad>Bogotá</ciudad>
</persona>
```

## Caso de Uso

Las aplicaciones web modernas utilizan APIs que intercambian información en formato JSON para enviar y recibir datos entre servidores y sistemas.





# C. Datos No Estructurados

Los datos no estructurados son aquellos que no poseen un formato definido ni están organizados en tablas. Representan la mayor parte de la información generada actualmente.

## Características

- No siguen una estructura fija.
- Son difíciles de almacenar en bases de datos tradicionales.
- Requieren herramientas especializadas para su análisis.
- Su procesamiento suele involucrar Inteligencia Artificial y Machine Learning.
- Contienen información valiosa que debe extraerse mediante técnicas avanzadas.

## Ejemplos

- Fotografías.
- Videos.
- Audios.
- Correos electrónicos.
- Publicaciones en redes sociales.
- Archivos PDF.
- Documentos Word.
- Imágenes médicas.
- Grabaciones de llamadas.

## Caso de Uso

Una empresa analiza comentarios de clientes en redes sociales para identificar sentimientos positivos o negativos sobre sus productos.

## Ejemplo

Una fotografía almacenada en formato JPG contiene millones de píxeles, pero no posee campos definidos como nombre, edad o ciudad. Por esta razón, se clasifica como un dato no estructurado.


# Resumen

- **Datos Estructurados:** Información organizada en tablas y fácil de consultar mediante SQL.
- **Datos Semiestructurados:** Información parcialmente organizada mediante etiquetas o claves, como JSON y XML.
- **Datos No Estructurados:** Información sin una estructura definida, como imágenes, videos, audios o documentos.

Comprender estos tipos de datos es fundamental para seleccionar las herramientas adecuadas de almacenamiento, procesamiento y análisis dentro de los proyectos de Analítica de Datos, Business Intelligence y Ciencia de Datos.