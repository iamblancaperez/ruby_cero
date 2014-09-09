# Introducción a Expresiones Regulares en Ruby

Ruby como otros lenguajes de scripting trae de manera integrada soporte a expresiones regulares. La expresiones regulares
en Ruby son un tipo de dato el cual debe declararse utilizando el "/".

Ejemplo

```ruby
/\d\d:\d\d:\d\d/    # Estructuras de tiempo como 12:24:50
/Ruby|Perl|Python/  # Busca coincidencia con la palabra Ruby o Perl o Python
```

Ruby no solo soporta los metodos básicos como son:

+ sub
+ gsub
+ match

Tambien permite la "comparación" directa que retorna un buleano.

```ruby
if "Este texto tiene la palabra Ruby" =~ /Ruby|Perl/
  puts "Eso es correcto"
else
  puts "No, no tiene la palabra"
end
```

```ruby
line = "Perl maneja de manera excelente las expresiones regulares"
line.sub(/Perl/, 'Ruby') # Sustituye la primera vez que se cumpla la expresion

# La función gsub, sustituye todas las ocurrencias de la expresion regular
```
