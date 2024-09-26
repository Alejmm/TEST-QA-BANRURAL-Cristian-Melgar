# Cristian Alejandro Melgar Ordoñez 
# Plan de Ataque
# Bugs Encontrados - Soluciones

## Bug 1. Generación incorrecta del número aleatorio
- **Descripción del Error:** El número aleatorio generado estaba limitado `Math.random() * 10`, en lugar de entre 0 y 100, no cumplia con el requisito.
- **Solución:** Modificar la línea del generador del número aleatorio `Math.floor(Math.random() * 100) + 1`, asegurando que el rango sea de 1 a 100.

## Bug 2. Validación de Entrada 
- **Descripción del Error:** No se verificaba si el valor ingresado por el usuario era un número entero válido entre 1 y 100, lo que podía causar errores en el juego.
- **Solución:** Agregar una verificación utilizando Number.isInteger(userGuess) y comprobar que el número esté en el rango adecuado (1 a 100). Si no es válido, se muestra una alerta y no se incrementa el intento.

## Bug 3. Eventos de escucha incorrectos
- **Descripción del Error:** Por escritur se utilizó incorrectamente addeventListener en lugar de addEventListener, lo que impedía que los eventos se registraran correctamente.
- **Solución:** Cambiar addeventListener a addEventListener en las líneas correspondientes para que los eventos se registren y respondan adecuadamente.

## Bug 4. Mensajes y colores de resultado incorrectos
- **Descripción del Error:** Los mensajes mostrados en respuesta no cumplían con los requisitos de color y texto especificados, estos se encontraban cruzados.
- **Solución:** Validar mensaje y color correspondiente para cada escenario.

## Bug 5. Reseteo del juego
- **Descripción del Error:** El número aleatorio no se regeneraba correctamente al reiniciar el juego.
- **Solución:** Asegurar de regenerar el número aleatorio al llamar a resetGame() usando randomNumber = Math.floor(Math.random() * 100) + 1.

## Bug 6. El campo no se limpiaba automaticamente
- **Descripción del Error:** El campo de entrada no se limpiaba luego de haber realizado un intento, se tenía que borrar e ingresar otro intento.
- **Solución:** Implementación de  `guessField.value = ''` para que después de cada intento se asegure que el campo sea limpiado.

## Bug 7. Cierre de etiqueta 
-**Descripción del Error:** Se valido que un cierre de etiqueta body se encontraba en un lugar no correspondiente.
-**Solución:** Colocar la etiqueta en el lugar correspondiente, para que el código estuviese dentro de la etiqueta.