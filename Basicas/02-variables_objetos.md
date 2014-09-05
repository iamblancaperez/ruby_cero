Intro a Ruby
============

Ruby es un lenguaje interpretado Orientado a Objetos no fuertemente tipado, por lo tanto todo es un objeto. Por lo tanto vamos a ver como funcionan alguna variables y tipos de datos basicos.

Para manejar este intro basico podemos usar el interprete interactivo de Ruby (irb).

Ya que, en ruby todo es un Objeto podemos observar desde el irb que los siguientes datos pueden usar el metodo "class" el cual retorna el tipo de objeto que es el dato.
Al mismo tiempo sobre cualquier objeto podemos usar el metodo "methods" el cual retorna todos los metodos que puede usar un objeto.

```ruby
2.1.1 :001 > 1.class
=> Fixnum
2.1.1 :002 > "Un string".class
=> String
2.1.1 :003 > [1,2,3,4,5].class
=> Array
2.1.1 :004 > 1.methods
 => [:to_s, :inspect, :-@, :+, :-, :*, :/, :div, :%, :modulo, :divmod, :fdiv, :**, :abs, :magnitude, :==, :===, :<=>, :>, :>=, :<, :<=, :~, :&, :|, :^, :[], :<<, :>>, :to_f, :size, :bit_length, :zero?, :odd?, :even?, :succ, :integer?, :upto, :downto, :times, :next, :pred, :chr, :ord, :to_i, :to_int, :floor, :ceil, :truncate, :round, :gcd, :lcm, :gcdlcm, :numerator, :denominator, :to_r, :rationalize, :singleton_method_added, :coerce, :i, :+@, :eql?, :remainder, :real?, :nonzero?, :step, :quo, :to_c, :real, :imaginary, :imag, :abs2, :arg, :angle, :phase, :rectangular, :rect, :polar, :conjugate, :conj, :between?, :nil?, :=~, :!~, :hash, :class, :singleton_class, :clone, :dup, :taint, :tainted?, :untaint, :untrust, :untrusted?, :trust, :freeze, :frozen?, :methods, :singleton_methods, :protected_methods, :private_methods, :public_methods, :instance_variables, :instance_variable_get, :instance_variable_set, :instance_variable_defined?, :remove_instance_variable, :instance_of?, :kind_of?, :is_a?, :tap, :send, :public_send, :respond_to?, :extend, :display, :method, :public_method, :singleton_method, :define_singleton_method, :object_id, :to_enum, :enum_for, :equal?, :!, :!=, :instance_eval, :instance_exec, :__send__, :__id__]>>]
```

En cuanto a la sintaxis basica en Ruby las variables solo deben indicar el nombre de la misma, no utiliza ningun otro caracter para definirla.

```ruby
2.1.1 :005 > un_string = "Sergio Marin"
=> "Sergio Marin"

2.1.1 :006 > un_integer = 123
=> 123

2.1.1 :007 > un_float = 123.123
=> 123.123

2.1.1 :009 > un_array = [1, "los arreglos", "soportan", "mezclar tipos de datos", 1234.4556]
=> [1, "los arreglos", "soportan", "mezclar tipos de datos", 1234.4556]

2.1.1 :012 > un_hash = {este_key: "Este es el valor", otro_key: "otro valor"}
=> {:este_key=>"Este es el valor", :otro_key=>"otro valor"}

```

Las constantes en Ruby se definen con el nombre de la misma toda en Mayuscula

```ruby
2.1.1 :010 > UNA_CONSTANTE = 2
=> 2
```

## Manejo de Arreglos

Los arreglos en Ruby como objeto de la clase Array tienen una serie de metodos, los cuales son muy utiles y permiten una cantidad de operaciones muy interesantes que nos pueden simplificar la vida.

```ruby
# definamos un array

2.1.1 :013 > un_array = [1, 2, 3, 4 ,5 ,6, 7 ,8 ,9 ,0]
=> [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]

2.1.1 :029 > un_array.size
=> 10

## Podemos tomar el valor de una posicion del arreglo de la siguiente manera

2.1.1 :014 > un_array[0]
=> 1

2.1.1 :015 > un_array[2]
=> 3

2.1.1 :016 > un_array[9]
=> 0

## Podemos vaciar el arreglo con el metodo clear

2.1.1 :017 > un_array.clear
=> []

## Si necesitamos ordenar el arreglo de manera invertida usamos el metodo .reverse, este metodo retorna el arreglo con el orden invertido, mas no modifica al arreglo original

2.1.1 :018 > un_array = [1, 2, 3, 4 ,5 ,6, 7 ,8 ,9 ,0]
=> [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]

2.1.1 :019 > un_array.reverse
=> [0, 9, 8, 7, 6, 5, 4, 3, 2, 1]

2.1.1 :020 > un_array.reverse[0]
=> 0

2.1.1 :021 > un_array.reverse[1]
=> 9

## Si necesitamos ordenar el arreglo de mayor a menor podemos usar el metodo sort

2.1.1 :022 > un_array.sort
=> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

## Si necesitamos borrar elementos de un arreglo existen dos metodos.

2.1.1 :023 > otro_array = [1, 2, 3, "cuatro", "cinco", "seis"]
=> [1, 2, 3, "cuatro", "cinco", "seis"]

# El delete_at elimina una posicion

2.1.1 :024 > otro_array.delete_at(3)
=> "cuatro"

2.1.1 :025 > otro_array
=> [1, 2, 3, "cinco", "seis"]

# El delete elimina un objeto dentro del array

2.1.1 :026 > otro_array.delete("seis")
=> "seis"

2.1.1 :027 > otro_array
=> [1, 2, 3, "cinco"]

```

Los hash en otros lenguejes como PHP son un array con key value. En ruby son un tipo de dato distinto.

```ruby

2.1.1 :030 > un_hash = {este_key: "Este es el valor", otro_key: "otro valor"}
=> {:este_key=>"Este es el valor", :otro_key=>"otro valor"}

2.1.1 :031 > un_hash[:este_key]
=> "Este es el valor"

2.1.1 :032 > un_hash[:otro_key]
=> "otro valor"

```

## Conclusion

En general este puede ser el uso de variables y tipos de datos basicos que podemos usar en Ruby.