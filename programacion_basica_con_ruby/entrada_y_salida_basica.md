# Entrada y Salida Basica

Los metodos de I/O son utilizados para leer y escribir, por lo general esta entrada/salida se dara en: la ejecucion de un script, lectura y escritura de un archivo y en el browser.

## En la ejecucion del script

Como hemos usado varias veces hasta ahora, en la ejecucion del script podemos usar el metodo puts para imprimir en pantalla el valor de una variable o objeto.

```ruby
puts "Hola mundo"
Hola mundo
```

Para poder obtener datos desde el teclado en la ejecucion del script, usamos el metodo 'gets'

```ruby
puts "Escriba un numero de veces"

veces = gets
i = 0

until i > veces.chomp.to_i
  puts "Veamos: #{i}"
  i += 1
end

```

## Conclusion

Nuestros script pueden tomar entrada desde el teclado en ejecucion y guardarlo en una variable para luego utilizarlo. Importante, la ejecucion queda pausada hasta que se escriba en el teclado la entrada y se presione ENTER.

El manejo de archivos lo realizaremos de manera mas detallada en otro tutorial.
