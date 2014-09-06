Bloques e iteradores
====================

Una de las fortalezas particulares de Ruby son los Bloques y los iteradores.
Juntos son unas de las herramientas mas utilizadas dentro del desarrollo con Ruby,
tanto que los iteradores en general son los encargados de sustituir a los metodos
para hacer ciclos (for, until, while, etc).

## Bloques

Los bloques no son mas, se pedazos de código que pueden ser guardados y ejecutados por
otra función. Los bloques de código pueden ser utilizados para implementar callbacks, pasar codigo como
parametro de una función y implementar los iteradores.

Existen dos maneras de definir un bloque en Ruby

```ruby
# Para bloques de una linea
{ puts "Esto es un bloque" }

# Para bloques multilinea
do
  suscripcion = curso.suscribir(alumno)
  alumno.socializar
  enviar_correo_de_notificacion(suscripcion)
end
```

Existen varias maneras de ejecutar un bloque cuando es pasado como una función,
la manera mas común de realizarlo es usando el metodo 'yield', el cual es un metodo
que ejecuta el contenido del bloque.

```ruby
# Sin parametros
def ejecutar_bloque
  puts "Comienza la ejecución del bloque"
  yield
  puts "Termina la ejecución del bloque"
end

ejecutar_bloque { puts "este es el contenido del bloque" }

# Con parametros globales de la funcion
def ejecutar_bloque_con_params_global(name, age)
  puts "Comienza la ejecución del metodo con paramatros"
  puts "El nombre es #{name}, y esta la edad #{age}"
  yield
  puts "Termina la ejecución del bloque"
end

ejecutar_bloque_con_params_global('Sergio', 29) { puts "este es el contenido del bloque" }

# Con paremetros que se van a usar dentro del bloque.
def ejecutar_bloque_con_params(name, age)
  puts "Comienza la ejecución del metodo con paramatros"
  yield(name, age)
  puts "Termina la ejecución del bloque"
end

ejecutar_bloque_con_params('Sergio', 29) do |nombre, edad|
  puts "El nombre que pasaron es: #{nombre}"
  puts "La edad es: #{edad}"
end
```

## Iteradores

Los iteradores son la manera en la que podemos realizar ciclos o iteraciones en la cual se ejecuta
un bloque.

Uno de los iteradores de uso común es el .each sobre un array o hash

```ruby
arreglo = %w(Sergio Oriana Jose Ciriaco Gustavo Erick Blanca)
arreglo.each do |nombre|
  puts "El nombre del usuario es: #{nombre}"
end
```
