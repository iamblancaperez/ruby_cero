Clases, Objetos y variables
===========================

Anteriormente habia mencionado que Ruby era un lenguaje orientado a objetos pero en los ejemplos anteriores no vimos el poder de esta orientación a objetos y como funciona.

## Clases

En Ruby las clases son las estructuras que se encargan de definir, los metodos, variables y acciones que puede realizar un Objeto. Como en otros lenguajes de programación.

Las clases se definen de la siguiente manera, ejemplo:

```ruby
class Persona
  # Si queremos definir el metodo constructor del objeto
  # Usaremos el metodo initialize, el cual se llama al instanciar
  # un objeto usando el Persona.new

  def initialize(name, age, id_number)
    # ...
  end
end
```

En Ruby existen 4 tipos de variables:

- **Variable local**: Tiene un scope local dentro de el metodo que la genera
- **Variable de instancia**: Tiene como scope todo el objeto instanciado
- **Variable de clase**: Tiene como scope la clase propiamente dicha, por lo tanto es compartida por todos los objetos instanciados de la misma clase.
- **Variable Global**: Es una variable que se mantiene en memoria mientras nuestro programa esta ejecución y es compartida por todos los metodos, clases dentro de la programa.

```ruby
$una_variable_global = "Las variables globales son malas, no las usen"
class Persona
  # Si queremos definir el metodo constructor del objeto
  # Usaremos el metodo initialize, el cual se llama al instanciar
  # un objeto usando el Persona.new
  @@cantidad_de_personas = 0
  def initialize(name, birthday, id_number)
    @name = name
    @birthday = birthday
    @id_number = id_number
    @@cantidad_de_personas = @@cantidad_de_personas - 1
  end

  def age
    days_between = (Date.today - birthday).to_i
    return days_between / 365
    # NOTA: en ruby no es necesario el return siempre y cuando
    # sea al final del metodo, ya que, hace un return implicito
    # del resultado de la ultima linea dentro de un metodo.
  end
end
```

En Ruby los metodos tienen 3 tipos de niveles/propiedades para control de acceso:

- Metodos Publicos: estos metodos pueden ser llamados por cualquiera.
- Metodos Protegidos: puede ser invocados por objetos de la clase definida o por algun objeto de una clase que herede de la primera.
- Metodos Privados: dichos metodos solo pueden ser llamados por otros metodos del mismo objeto.

```ruby
class Animal
  def metodo_publico
    puts 'esto es un metodo publico'
  end

  protected
  def metodo_protegido
    puts 'esto es un metodo protegido'
  end

  private
  def metodo_privado
    puts 'esto es un metodo privado'
  end
end
```

### Herencia

En Ruby solo existe la herencia unica, es decir una clase solo puede heredar propiedades, de una unica clase.

Ejemplo:

```ruby
class Animal
  def initialize(patas, cabeza)
    @patas, @cabeza = patas, cabeza # asignación de multiples variables en una sola linea
  end
end

class Perro < Animal
  def initialize
    super(4, 1) # El metodo super es un metodo que hace llamado al new de la clase "padre"
  end
end
```
