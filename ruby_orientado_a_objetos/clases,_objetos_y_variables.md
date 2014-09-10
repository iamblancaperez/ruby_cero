# Clases, Objetos y variables

Anteriormente había mencionado que Ruby era un lenguaje orientado a objetos pero en los ejemplos anteriores no vimos el poder de esta orientación a objetos y como funciona.

## Clases

En Ruby las clases son las estructuras que se encargan de definir, los métodos, variables y acciones que puede realizar un Objeto. Como en otros lenguajes de programación.

Las clases se definen de la siguiente manera, ejemplo:

```ruby
class Persona
  # Si queremos definir el método constructor del objeto
  # Usaremos el método initialize, el cual se llama al instanciar
  # un objeto usando el Persona.new

  def initialize(name, age, id_number)
    # ...
  end
end
```

En Ruby existen 4 tipos de variables:

- **Variable local**: Tiene un scope local dentro de el método que la genera
- **Variable de instancia**: Tiene como scope todo el objeto instanciado
- **Variable de clase**: Tiene como scope la clase propiamente dicha, por lo tanto es compartida por todos los objetos instanciados de la misma clase.
- **Variable Global**: Es una variable que se mantiene en memoria mientras nuestro programa esta ejecución y es compartida por todos los métodos, clases dentro de la programa.

```ruby
$una_variable_global = "Las variables globales son malas, no las usen"
class Persona
  # Si queremos definir el método constructor del objeto
  # Usaremos el método initialize, el cual se llama al instanciar
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
    # sea al final del método, ya que, hace un return implícito
    # del resultado de la última línea (operación) dentro de un método.
  end
end
```

En Ruby los métodos tienen 3 tipos de niveles/propiedades para control de acceso:

- Métodos Públicos: estos métodos pueden ser llamados por cualquiera.
- Métodos Protegidos: puede ser invocados por objetos de la clase definida o por algun objeto de una clase que herede de la primera.
- Metodos Privados: dichos métodos solo pueden ser llamados por otros métodos del mismo objeto.

```ruby
class Animal
  def metodo_publico
    puts 'esto es un método publico'
  end

  protected
  def metodo_protegido
    puts 'esto es un método protegido'
  end

  private
  def metodo_privado
    puts 'esto es un método privado'
  end
end
```

### Herencia

En Ruby solo existe la herencia única, es decir una clase sólo puede heredar propiedades, de una única clase.

Ejemplo:

```ruby
class Animal
  def initialize(patas, cabeza)
    @patas, @cabeza = patas, cabeza # asignación de multiples variables en una sola linea
  end
end

class Perro < Animal
  def initialize
    super(4, 1) # El método super es un método que hace llamado al new de la clase "padre"
  end
end
```
