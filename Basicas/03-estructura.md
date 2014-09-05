Estructuras de Control de Ruby
==============================

Ruby ofrece diferentes estructuras de control que nos permiten alterar el flujo de la ejecución del programa, entre ellas podemos destacar:

* if
* unless
* case

En este caso no usaremos la consola interactiva para probar nuestro codigo, sino. Que crearemos un archivo con la extension “.rb” para nuestras pruebas.

### IF

Primer archivo: prueba_if.rb

```ruby
#!/usr/bin/ruby

nombre = "Sergio Marin"

if nombre == "Sergio Marin"
	puts "El nombre es Sergio Marin"
else
	puts "El no es Sergio Marin"
end

# En caso de necesitar el else if en ruby se usa la siguiente sintaxis

numero = 3

if numero > 5
	puts  "#{numero} es mayor que 5"
elsif numero == 3
	puts "#{numero} es igual a 3"
else
	puts "#{numero} es menor que 5 pero no es igual a 3"
end
```

Para correr el script desde la consola

```bash
ruby ~/Desktop/prueba_if.rb

El nombre es Sergio Marin
El numero es igual a 3
```

### UNLESS

La estructura de control UNLESS, es similar a el IF en cuanto a estructura pero solo ejecuta el codigo si no es igual a la condición

```bash
#!/usr/bin/ruby

numero = 1
unless numero == 1
	puts "El numero no es el 1"
else
	puts "El numero es el 1"
end
```

La respuesta en este caso sera:

```bash
ruby ~/Desktop/prueba_unless.rb

El numero es el 1
```

### Case

En caso de tener una variable que necesitamos comprobar muchos casos, en vez de usar muchos if con elsif, seria mas natural usar la expresion case

```ruby
case variable
when [condicion]
	# code
when [condicion]
	# code
else
	# code
end
```
Un ejemplo mas claro del uso del case pude ser:

```ruby
#!/usr/bin/ruby

edad =  5
case edad
when 0 .. 2
	puts "Bebe"
when 3 .. 12
	puts "Niño"
 when 13 .. 18
	puts "Adolescente"
else
	puts "Adulto"
end
```
