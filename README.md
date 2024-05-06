# Conversor de Moneda

Este proyecto es una aplicación Java que permite al usuario convertir entre diferentes monedas utilizando un servicio de tasas de cambio en línea.

## Estructura del Proyecto

El proyecto consta de un archivo principal llamado `Main.java`. Este archivo contiene el código fuente de la aplicación Java.

## Funcionalidades

1. **Menú Principal:**
   - Al iniciar la aplicación, se muestra un menú principal que ofrece tres opciones al usuario: "Convertir moneda", "Consultar historial" y "Salir".
   - El usuario puede seleccionar una de estas opciones utilizando el cuadro de diálogo proporcionado por `JOptionPane`.
   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/e094ca77-c202-4c54-b300-e84d642d2d3b)


2. **Convertir Moneda:**
   - Cuando el usuario elige la opción "Convertir moneda" en el menú principal, se le solicita que seleccione la moneda de origen y la moneda de destino utilizando cuadros de diálogo `JOptionPane`.
   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/cf45cd26-0d3f-446f-957a-6b434949a9fe)

   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/4cfb63a8-9273-4b6d-8b50-e108e69de730)


   - Luego, se le pide al usuario que ingrese la cantidad que desea convertir.
   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/69319dcc-5e1c-4042-960a-7c314ec72367)

   - La aplicación utiliza un servicio de tasas de cambio en línea para obtener la tasa de conversión entre las dos monedas seleccionadas.
   - Después de realizar la conversión, se muestra el resultado al usuario en otro cuadro de diálogo `JOptionPane`.
   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/03a59179-ceba-4d17-a70f-d1db3c1c2030)

   - Si el usuario elige, puede convertir otra cantidad con las mismas monedas de origen y destino seleccionadas anteriormente.
   - ![image](https://github.com/carsalan1/Conversor/assets/99160256/6a5fb200-70ed-4b8b-98d9-4e39c337d478)

      ![image](https://github.com/carsalan1/Conversor/assets/99160256/ae606e38-1623-4160-b248-3364a7487427)


3. **Consultar Historial:**
   - Cuando el usuario elige la opción "Consultar historial" en el menú principal, se muestra un cuadro de diálogo `JOptionPane` con el historial de conversiones recientes.
   - El historial se almacena en una lista y se muestra al usuario en el cuadro de diálogo.
        
![image](https://github.com/carsalan1/Conversor/assets/99160256/3f91a3d7-085a-451c-b3ff-b5fdaa0a188b)


4. **Salir del Programa:**
   - Si el usuario elige la opción "Salir" en el menú principal, el programa se cierra.

## Integración con Servicio de Tasa de Cambio

- La aplicación utiliza un servicio de tasas de cambio en línea para obtener las tasas de conversión entre diferentes monedas.
- Se hace una solicitud HTTP al servicio utilizando la URL proporcionada con la moneda base como parámetro.
- La respuesta se analiza para obtener las tasas de conversión y se utiliza para realizar las conversiones de moneda.
- El servicio en línea utilizado para obtener las tasas de cambio es ExchangeRate-API. Este servicio proporciona datos precisos y actualizados sobre las tasas de cambio entre diferentes monedas.

URL para las Tasas de Cambio:
La URL para acceder a las tasas de cambio proporcionadas por ExchangeRate-API es la siguiente:
https://v6.exchangerate-api.com/v6/{API_KEY}/latest/{BASE_CURRENCY}

{API_KEY}: Se refiere a la clave de API proporcionada por ExchangeRate-API. Debes registrarte en su plataforma para obtener tu propia clave de API.
{BASE_CURRENCY}: Especifica la moneda base para la cual se desean obtener las tasas de cambio. En el código proporcionado, se utiliza la moneda base dinámicamente basada en la selección del usuario.
La API responde con un objeto JSON que contiene las tasas de cambio entre la moneda base especificada y otras monedas.

Por ejemplo, si {API_KEY} es "YOUR_API_KEY" y {BASE_CURRENCY} es "USD" (dólar estadounidense), la URL sería:
https://v6.exchangerate-api.com/v6/YOUR_API_KEY/latest/USD
Al hacer una solicitud GET a esta URL, obtendrás un objeto JSON que contiene las tasas de cambio para el dólar estadounidense en relación con otras monedas.
