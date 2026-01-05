# Regresion-Testing-Urban-Routes
Proyecto 1 

# Informe de Pruebas de Regresión - Urban Routes

## Introducción

El presente informe describe los hallazgos de las pruebas de regresión ejecutadas para la aplicación Urban Routes, un sistema de mapeo y navegación urbana. El análisis se fundamenta en la realización de 24 casos de prueba, cuyos datos se registran en un archivo con dos hojas principales: "Casos de prueba" e "Informes de errores".

<a href="https://docs.google.com/spreadsheets/d/1qaMxFPK7l_3kuFnoM3rSNRwvstR4caIm/edit?usp=drive_link&ouid=106582061342206139422&rtpof=true&sd=true" target="_blank">
 📊​ Archivo original 
</a>

## Proceso

Las pruebas se realizaron mediante un enfoque sistemático que cubrió:

1. **Validación de Funcionalidades Base**:
   - Desplazamiento y zoom en el mapa
   - Funcionalidad de búsqueda de direcciones
   - Interactividad con los elementos del mapa
   - Opciones de vista (satelital, relieve, pantalla completa)

3. **Metodología de Pruebas**:
   - Se llevaron a cabo pruebas de regresión para confirmar la estabilidad de funciones preexistentes
   - Cada caso de prueba fue registrado con:
     - Condiciones iniciales
     - Pasos detallados de ejecución
     - Resultados esperados
     - Estado final de la prueba
   - Los errores encontrados fueron categorizados por severidad (Bloqueador, Crítico, Grave, Menor, Trivial)

4. **Documentación y Seguimiento**:
   - Se reportaron 7 incidencias con su nivel de severidad y una descripción completa
   - Los casos fallidos se asociaron con un ID único para facilitar su seguimiento
   - Se agregaron observaciones específicas para situaciones particulares

Los resultados de las pruebas revelaron tanto problemas críticos como menores, los cuales impactan tanto la funcionalidad principal como aspectos secundarios de la aplicación. Estos hallazgos ofrecen una base confiable para priorizar las correcciones requeridas y garantizar la calidad del producto.

# Resumen de Casos de Prueba - Urban Routes

## Datos Generales
| Categoría | Detalle |
|-----------|---------|
| Probador | Alejandro Vázquez Guerrero |
| Aplicación | Urban Routes |
| Total de Casos | 24 |

## Estado de los Casos
| Estado | Cantidad |
|--------|-----------|
| Aprobados | 14 |
| No Aprobados | 7 |
| Omitidos | 3 |

## Detalle de Casos de Prueba

| ID | Título | Condición Previa | Resultado Esperado | Estado | ID Error |
|------|---------|------------------|-------------------|---------|-----------|
| CASO-1 | Desplazamiento del mapa | Abrir la aplicación Urban Routes | El mapa se mueve. Todos los objetos se muestran según el diseño. | Aprobado | - |
| CASO-2 | Zoom del mapa | La aplicación Urban Routes no debe estar abierta | El nivel de zoom aumenta en un valor. Todos los objetos se muestran según el diseño. | Aprobado | - |
| CASO-3 | No se puede hacer clic en los encabezados del área en el mapa | Abrir la aplicación Urban Routes | No ocurre nada. Los usuarios no pueden interactuar con los encabezados del mapa. | No aprobado | BR1 |
| CASO-4 | No se puede hacer clic en los encabezados de la ciudad en el mapa | Abrir la aplicación Urban Routes | No ocurre nada. Los encabezados de la ciudad no se pueden seleccionar. | Aprobado | - |
| CASO-5 | Se puede seleccionar el campo "Desde" | Abrir la aplicación Urban Routes | Se selecciona el campo "Desde". El cursor parpadea. El campo de búsqueda está vacío. | No aprobado | BR2 |
| CASO-6 | Se pueden buscar objetos en el campo "Hasta" | Abrir la aplicación Urban Routes | Se muestra la lista de estaciones de metro. | No aprobado | BR3 |
| CASO-7 | El pin de la dirección aparece después de completar el campo "Desde" | Abrir la aplicación Urban Routes | El mapa hace zoom sobre el pin de la dirección seleccionada. La vista coincide con la descripción del diseño. | No aprobado | BR4 |
| CASO-8 | El pin de la dirección aparece después de completar el campo "Hasta" | Abrir la aplicación Urban Routes | El mapa hace zoom sobre el pin de la dirección seleccionada. | No aprobado | BR5 |
| CASO-9 | La dirección se elimina después de borrar el campo "Desde" | Abrir la aplicación Urban Routes. El campo "Desde" debe estar lleno | El campo está vacío. La dirección introducida anteriormente se ha eliminado del campo. La marca correspondiente desaparece del mapa. | Omitido | - |
| CASO-10 | La dirección se elimina después de borrar el campo "Hasta" | Abrir la aplicación Urban Routes. El campo "Hasta" debe estar lleno | El campo está vacío. La dirección introducida anteriormente se ha eliminado del campo. La marca correspondiente desaparece del mapa. | Omitido | - |
| CASO-11 | Se muestran los objetos 3D | Abrir la aplicación Urban Routes | El objeto se renderiza en 3D. | Aprobado | - |
| CASO-12 | El modo de vista de pantalla completa se activa al hacer clic en el botón del modo de vista de pantalla completa | Abrir la aplicación Urban Routes. El modo de vista de pantalla completa no debe estar activado | El modo de vista de pantalla completa se activa y las pestañas del navegador se ocultan. Todos los objetos de la interfaz del mapa están en su lugar. El nivel de zoom no cambia. | No aprobado | BR6 |
| CASO-13 | El modo de vista de pantalla completa se desactiva al hacer clic de nuevo en el botón del modo de vista de pantalla completa | Abrir la aplicación Urban Routes. Activar el modo de vista de pantalla completa | El modo de vista de pantalla completa se desactiva y las pestañas del navegador se vuelven a mostrar. Todos los objetos de la interfaz del mapa están en su lugar. El nivel de zoom no cambia. | Aprobado | - |
| CASO-14 | El modo Relieve se activa al hacer clic en el botón del modo Relieve | Abrir la aplicación Urban Routes | La casilla de verificación se rellena. El mapa se muestra en modo Relieve y coincide con el diseño. | Aprobado | - |
| CASO-15 | El modo Satélite se activa al hacer clic en el botón del modo Satélite | Abrir la aplicación Urban Routes | El mapa muestra el modo Satélite. La vista no tiene problemas notables. | Aprobado | - |
| CASO-16 | Los edificios se muestran al hacer zoom sobre ellos | Abrir la aplicación Urban Routes | El edificio se muestra según el diseño. | Aprobado | - |
| CASO-17 | Las estaciones de metro se muestran al hacer zoom sobre ellas | Abrir la aplicación Urban Routes | Se muestra el ícono del metro. | Aprobado | - |
| CASO-18 | Los lugares de interés se muestran al hacer zoom sobre ellos | Abrir la aplicación Urban Routes | Se muestra el ícono del lugar de interés. | Aprobado | - |
| CASO-19 | Los parques se muestran al hacer zoom sobre ellos | Abrir la aplicación Urban Routes. | Se muestra el ícono del parque. | Aprobado | - |
| CASO-20 | La información del objeto se muestra al hacer clic en un objeto | Abrir la aplicación Urban Routes. | La visualización de información (con información del lugar) está abierta. La vista coincide con el diseño. | Aprobado | - |
| CASO-21 | La información del objeto se oculta al hacer clic en la cruz en la vista de información | Abrir la aplicación Urban Routes | La vista de información está cerrada. No hay elementos adicionales en el mapa. | Aprobado | - |
| CASO-22 | El modo Street View se activa cuando el ícono de Street View se arrastra sobre una calle | Abrir la aplicación Urban Routes. El modo Street View no debe estar activado | El modo Street View se activa. La imagen se desplaza 360 grados. | Omitido | - |
| CASO-23 | El modo Street View se desactiva al hacer clic en una flecha gris | Abrir la aplicación Urban Routes. Activar el modo Street View | El modo Street View se desactiva. | Aprobado | - |
| CASO-24 | La información de la aplicación se muestra al hacer clic en el logotipo de la aplicación | Abrir la aplicación Urban Routes | Se muestra la información sobre la aplicación. | No aprobado | BR7 |

## Resumen de Errores Encontrados
| ID Error | Descripción |
|----------|-------------|
| BR1 | Error en interacción con encabezados de área |
| BR2 | Error en selección del campo "Desde" |
| BR3 | Error en búsqueda del campo "Hasta" |
| BR4 | Error en visualización del pin de dirección (Desde) |
| BR5 | Error en visualización del pin de dirección (Hasta) |
| BR6 | Error en modo pantalla completa |
| BR7 | Error en visualización de información de la aplicación |

# Informe de Errores - Urban Routes

## Resumen de Severidades
| Severidad | Cantidad |
|-----------|----------|
| Bloqueador | 0 |
| Crítico | 3 |
| Grave | 2 |
| Menor | 2 |
| Trivial | 0 |

## Detalle de Errores

| ID | Título | Severidad | Resultado Esperado | Resultado Actual |
|------|---------|------------|-------------------|-----------------|
| BR1 | Los encabezados de áreas no responden al clic en el mapa. | Menor | No ocurre nada. Los usuarios no pueden interactuar con los encabezados del mapa. | Se muestra un cuadro de diálogo con la información del encabezado. |
| BR2 | El campo "Desde" muestra una sugerencia en lugar de estar vacío al seleccionarlo. | Menor | Se selecciona el campo "Desde". El cursor parpadea. El campo de búsqueda está vacío. | Al seleccionar el campo "Desde": El cursor parpadea. El campo de búsqueda muestra una sugerencia. |
| BR3 | No se ejecutan búsquedas al introducir texto en el campo "Hasta". | Crítico | Se muestra la lista de estaciones de metro. | No ocurre ninguna búsqueda en el campo "Hasta", al introducir algún valor. |
| BR4 | El mapa no muestra pin ni hace zoom al ingresar dirección en el campo "Desde". | Crítico | El mapa hace zoom sobre el pin de la dirección seleccionada. La vista coincide con la descripción del diseño. | Al ingresar una dirección en el campo "Desde", Urban Routes no realiza ninguna acción. |
| BR5 | El mapa no muestra pin ni hace zoom al ingresar dirección en el campo "Hasta". | Crítico | El mapa hace zoom sobre el pin de la dirección seleccionada. La vista coincide con la descripción del diseño. | El mapa no realiza ninguna acción al ingresar una dirección en el campo "Hasta". |
| BR6 | Elementos de IU desaparecen al activar modo pantalla completa. | Grave | El modo de vista de pantalla completa se activa y las pestañas del navegador se ocultan. Todos los objetos de la interfaz del mapa están en su lugar. El nivel de zoom no cambia. | Al activar el modo de pantalla completa, algunos objetos de la interfaz desaparecen, tales como el logo y los campos "Desde" y "Hasta". |
| BR7 | No se muestra información de la aplicación al hacer clic en el logotipo. | Grave | Se muestra la información sobre la aplicación. | No se muestra información alguna. |

## Distribución de Errores por Funcionalidad

| Funcionalidad | Cantidad de Errores |
|---------------|-------------------|
| Búsqueda y Navegación | 4 |
| Interfaz de Usuario | 2 |
| Interacción con Mapa | 1 |
