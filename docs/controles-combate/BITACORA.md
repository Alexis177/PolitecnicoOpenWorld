# Bitácora de la contribución

**Autor:** David Alexis Hernandez Gonzalez (Alexis177)  
**Boleta:** 2024630227  
**Grupo:** 7CV4  
**Rama:** `fix/tamano-controles-combate`

Esta bitácora resume el trabajo realizado. No se registraron horarios individuales de las actividades.

| Etapa | Actividad | Resultado o evidencia |
| --- | --- | --- |
| Preparación | Crear el fork y abrir el proyecto en Android Studio. | Fork en Alexis177/PolitecnicoOpenWorld. |
| Ejecución inicial | Ejecutar el juego en el teléfono. | Aplicación ejecutada en Samsung Galaxy S22 Ultra. |
| Identificación | Detectar que el tamaño configurado no afectaba al modo de combate. | Se definió reutilizar la preferencia de tamaño existente. |
| Rama | Crear una rama para la corrección. | fix/tamano-controles-combate. |
| Implementación | Leer la preferencia en Android y pasarla a la pantalla común. | StreetFighterScreenAndroid.kt y StreetFighterScreen.kt. |
| Ajuste visual | Aplicar la escala al joystick, botones, separaciones e indicación del tutorial. | Commit 5cd5883: 2 archivos, 47 líneas añadidas y 20 eliminadas. |
| Pruebas manuales | Comparar 60 % y 100 %, probar respuesta y reinicio. | El autor confirmó funcionamiento y persistencia; no observó superposiciones ni recortes en los escenarios probados. |
| Publicación de código | Guardar el commit y hacer push al fork. | Commit 5cd5883 disponible en la rama de trabajo. |
| Documentación | Preparar informe, cinco capturas y esta bitácora en español. | README.md, BITACORA.md y carpeta capturas. |
| Preparación del PR | Redactar título y descripción en inglés con las cuatro secciones solicitadas. | PR_TITLE.txt y PR_DESCRIPTION.md. |

## Pendiente de entrega

1. Hacer commit y push de esta documentación.
2. Crear el PR hacia el repositorio original con el título y la descripción preparados.
3. Registrar la liga del PR en la entrega del examen.

El PR todavía no se ha creado como parte de esta preparación. El informe contiene los límites de las pruebas realizadas y las evidencias visuales.
