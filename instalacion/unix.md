Instalación de Ruby con RVM para Linux/Mac
==========================================

Los interpretes de Ruby tienen distintas maneras de ser instalados y de manejar sus versiones, por ejemplo en Ubuntu puede instalarse desde el manejador de paquetes (apt-get). Pero esto nos instalara un version especifica de Ruby y no nos permite manejar versiones distintas.

Utilizando rvm podemos ademas de instalar ruby manejar sus distintas versiones y implementaciones.

Para instalar rvm necesitamos contar con el comando curl o wget para descargar el instalador.

#### En linux (Derivados de Debian)

```bash
sudo apt-get install curl wget
```

#### En OSX (en caso que no este preinstalado)

```bash
brew install curl
```

Luego de tener curl instalado podemos proceder a instalar rvm

```bash
\curl -L https://get.rvm.io | bash -s stable
echo ‘[[ -s “$HOME/.rvm/scripts/rvm” ]] && source “$HOME/.rvm/scripts/rvm”  >> ~/.bashrc
```
Luego de terminar este proceso debemos cerrar la consola y volver a abrir para que cargue RVM, ya con RVM funcionando debemos instalar las dependencias necesarias para compilar Ruby

```bash
rvm requirements
```

Luego de instalar todos los requerimientos finalmente podemos instalar la version de ruby que queramos. Ejemplo:

```bash
rvm install 2.1.2
rvm use 2.1.1 --default
rvm rubygems current
```
Luego podemos instalar Ruby on Rails:

```bash
rvm install rails --no-doc --no-ri
```
