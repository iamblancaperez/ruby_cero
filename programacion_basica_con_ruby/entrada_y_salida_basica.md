# Entrada y Salida Básica

Los métodos de I/O son utilizados para leer y escribir, por lo general esta entrada/salida se dará en casos como: la ejecución de un script, lectura y escritura de un archivo y en el browser.

## En la ejecución del script

Como hemos usado varias veces hasta ahora, en la ejecución del script podemos usar el método puts para imprimir en pantalla el valor de una variable o objeto.

```ruby
puts "Hola mundo"
Hola mundo
```

Para poder obtener datos desde el teclado en la ejecución del script, usamos el método 'gets'

```ruby
puts "Escriba un número de veces"

veces = gets
i = 0

until i > veces.chomp.to_i
  puts "Veamos: #{i}"
  i += 1
end

```

## Conclusión

Nuestros script pueden tomar entrada desde el teclado en ejecución y guardarlo en una variable para luego utilizarlo. Importante, la ejecución queda pausada hasta que se escriba en el teclado la entrada y se presione ENTER.

El manejo de archivos lo realizaremos de manera mas detallada en otro tutorial.
