# Instalación

Ruby es un lenguaje de scriping multi plataforma, por ser un lenguaje de scripting los documentos se escriben como un documento de texto plano con extension .rb y son ejecutados por un interprete. En ruby existen multiples interpretes, pero en principio instalaremos el interprete basico.

Para realizar la instalación del interprete usaremos RVM (Ruby Version Manager) el cual permite instalar y manegar distintas versiones de Ruby sin que eso represente un problema de compatibilidad dentro de nuestro sistema operativo.

## Instalación de RVM

RVM trabaja en sistema basados en Unix como son: Linux y Mac OSX. Por lo tanto uno de los requisitos para el libro y el curso es contar con un sistema operativo Linux o Mac OSX. 

La instalación de RVM se realiza descargando un script desde su sitio web, para poder realizar esa descarga debemos tener instalado en nuestro sistema operativo una herramienta llamada curl.

En caso de usar Ubuntu o alguna distribución linux basada en debian, debemos asegurarnos de tener instalado curl y para eso podemos usar el siguiente comando:

#### En linux (Derivados de Debian)

```bash
sudo apt-get install curl wget
```

#### En OSX (en caso que no este preinstalado)

```bash
brew install curl
```

Y para instalar el RVM propiamente dicho usaremos:

```bash
\curl -L https://get.rvm.io | bash -s stable
echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"'  >> ~/.bashrc
```

## Instalación de Ruby

Luego de terminar este proceso debemos cerrar la consola y volver a abrir para que cargue RVM, ya con RVM funcionando debemos instalar las dependencias necesarias para compilar Ruby.

```bash
rvm requirements
```

Luego de instalar todos los requerimientos finalmente podemos instalar la version de ruby que queramos. 

Ejemplo:

```bash
rvm install 2.1.2
rvm use 2.1.1 --default
rvm rubygems current
```
### Como correr ruby

Existen muchas maneras de correr codigo Ruby, las dos mas comunes son:

- Utilizando la consola interactiva de Ruby
- Ejecutando el archivo con el interprete

Para usar la consola usarmos el comando 'irb'

```bash
irb
```
La consola interactiva permite evaluar codigo Ruby de manera dinamica.

Ejemplo:

```irb
2.1.1 :001 > "Hola mundo, desde el irb"
 => "Hola mundo, desde el irb"
```
La primera linea esta computa de un promt, el cual muestra la version de Ruby (en este caso 2.1.1) y la linea que se esta evaluando. Luego de evaluar el codigo que le presentemos nos retorna con '=>'.

Y para ejecutar un archivo

```bash
ruby nombre_del_archivo.rb
```




