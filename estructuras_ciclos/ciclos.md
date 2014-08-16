Ciclos
======

Los ciclos o bucles se utilizan para ejecutar un bloque de codigo una cantidad limitada de veces. Es importante que la condicion de parada del ciclo este bien definida para el ciclo pare, en caso contrario quedara en un ciclo infinito.

## WHILE

El ciclo while ejecuta un bloque de codigo mientras la condicion retorne TRUE

```ruby
#!/usr/bin/ruby

iterador = 0

while iterador <  5  do
  puts "el número es: #{numero}"
  iterador = iterador + 1
end
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_while.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
```

## REPEAT

El repeat funciona de manera similar a el while pero la condicion se ejecuta al final del bloque

```ruby
#!/usr/bin/ruby

iterador = 0

begin
  puts "el número es: #{numero}"
  iterador += 1
end while iterador <  5
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_repeat.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
```

## UNTIL

El until ejecuta un bloque de codigo hasta que se cumpla la condicion, es decir, hasta que la condicion retorne TRUE

```ruby
#!/usr/bin/ruby

iterador = 0

until iterador > 5
  puts "el número es: #{iterador}"
  iterador += 1
end
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_until.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
el número es: 5
```

## FOR

El metodo for ejecuta un bloque de codigo por cada elemento dentro de un rango o un array (el rango y el array no son lo mismo)

Ejemplo

```ruby
#!/usr/bin/ruby

for i in 0..5
  puts "El valor de la variable es: #{i}"
end

puts 'En caso de ser un arreglo'
arreglo = ['uno', 'dos', 'tres', 'cuatro', 'cinco', 'seis']

for i in arreglo
  puts "El valor de la variable es: #{i}"
end
```

El resultado de ejecutar este archivo seria.

```bash
ruby ~/Desktop/ejemplo_for.rb

El valor de la variable es: 0
El valor de la variable es: 1
El valor de la variable es: 2
El valor de la variable es: 3
El valor de la variable es: 4
El valor de la variable es: 5
En caso de ser un arreglo
El valor de la variable es: uno
El valor de la variable es: dos
El valor de la variable es: tres
El valor de la variable es: cuatro
El valor de la variable es: cinco
El valor de la variable es: seis
```

## Conclusion

En ruby podemos ejecutar un codigo N cantidad de veces usando las estructuras ya conocidas de ciclos, aunque en Ruby generalmente estos ciclos no son usados regularmente
