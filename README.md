# Conversor de Moneda

Este proyecto es una aplicación Java que permite al usuario convertir entre diferentes monedas utilizando un servicio de tasas de cambio en línea.

## Estructura del Proyecto

El proyecto consta de un archivo principal llamado `Main.java`. Este archivo contiene el código fuente de la aplicación Java.

## Funcionalidades

1. **Menú Principal:**
   - Al iniciar la aplicación, se muestra un menú principal que ofrece tres opciones al usuario: "Convertir moneda", "Consultar historial" y "Salir".
   - El usuario puede seleccionar una de estas opciones utilizando el cuadro de diálogo proporcionado por `JOptionPane`.

2. **Convertir Moneda:**
   - Cuando el usuario elige la opción "Convertir moneda" en el menú principal, se le solicita que seleccione la moneda de origen y la moneda de destino utilizando cuadros de diálogo `JOptionPane`.
   - Luego, se le pide al usuario que ingrese la cantidad que desea convertir.
   - La aplicación utiliza un servicio de tasas de cambio en línea para obtener la tasa de conversión entre las dos monedas seleccionadas.
   - Después de realizar la conversión, se muestra el resultado al usuario en otro cuadro de diálogo `JOptionPane`.
   - Si el usuario elige, puede convertir otra cantidad con las mismas monedas de origen y destino seleccionadas anteriormente.

3. **Consultar Historial:**
   - Cuando el usuario elige la opción "Consultar historial" en el menú principal, se muestra un cuadro de diálogo `JOptionPane` con el historial de conversiones recientes.
   - El historial se almacena en una lista y se muestra al usuario en el cuadro de diálogo.

4. **Salir del Programa:**
   - Si el usuario elige la opción "Salir" en el menú principal, el programa se cierra.

## Integración con Servicio de Tasa de Cambio

- La aplicación utiliza un servicio de tasas de cambio en línea para obtener las tasas de conversión entre diferentes monedas.
- Se hace una solicitud HTTP al servicio utilizando la URL proporcionada con la moneda base como parámetro.
- La respuesta se analiza para obtener las tasas de conversión y se utiliza para realizar las conversiones de moneda.
