# Informe de Corrección de Código

## Autor: Luis Carlos Estrada  
## Fecha de Compromiso: 1 de abril de 2025  

## Resumen
Se realizaron diversas correcciones al código del juego "Adivina tu número" para solucionar problemas de lógica, errores en la estructura y mejorar la funcionalidad general. A continuación, se detallan los cambios efectuados.

## Cambios Realizados

 **1. Generación de Número Aleatorio Incorrecta**
- **Problema:** La función resetGame solo obtenía un 1 como número aleatorio.
- **Solución:** Se corrigió la asignación de randomNumber para que genere un número entero entre 1 y 100 correctamente.

 **2. Lógica Incorrecta en Mensajes de Victoria y Derrota**
- **Problema:** El mensaje de victoria se mostraba cuando se perdía y viceversa.
- **Solución:** Se invirtieron las condiciones lógicas en la función checkGuess() para que los mensajes se muestren de forma correcta.

 **3. Uso Incorrecto de EventListener y Tipo de Dato en input**
- **Problema:**
  - addeventListener estaba mal escrito (debía ser addEventListener).
  - El input del número no se parseaba a tipo number, lo que provocaba errores de comparación.
- **Solución:**
  - Se corrigió la sintaxis de addEventListener.
  - Se agregó Number(guessField.value) en checkGuess() para convertir la entrada en un número válido.

 **4. Falta del Carácter . para Selección de Clases**
- **Problema:** Se omitió el carácter . en la selección de .lowOrHi, causando que document.querySelector('lowOrHi') fallara.
- **Solución:** Se corrigió a document.querySelector('.lowOrHi').

 **5. Número Aleatorio Incorrectamente Generado**
- **Problema:**
  - Se generaba un número decimal entre 0 y 10 en lugar de un número entero entre 1 y 100.
- **Solución:** Se usó Math.floor(Math.random() * 100) + 1 para asegurar un número entero dentro del rango adecuado.