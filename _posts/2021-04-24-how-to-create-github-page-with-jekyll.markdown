---
layout: post
title:  "Como crear una página web en Github con Jekyll"
date:   2021-04-24 19:04:30 -0400
categories: jekyll
---

Bienvenido a mi primer post en el blog que acabo de crear, aprovechando esta rueda de motivación y con los conceptos frescos, que mejor que un tutorial de como puedes crear tu propio blog o página personal en github. 

Este post tiene como objetivo ayudar en los primeros pasos y configuraciones necesarias para ver tu página en la web. Seguire subiendo contenido a medida que desarrolle mi propia página web. Probablemente este post sea uno de muchos en una sección de mi perfil.


## Pre-requisitos
1. Tener un editor de texto como Visual Studio Code
2. Tener Ruby instalado en su versión 2.4.0 o superior (puedes confirmarla con el comando `ruby -v`)
3. Tener instaldo Jekyll (con ruby istalado ejecutar `gem install bundler jekyll`)

[jekyll-pre-requisitos]: https://jekyllrb.com/docs/installation/


## Pasos

### Creación de un repositorio en Github
1. Ir a Github, crear un repositorio vacio o con un Readme, el nombre del repositorio influira en la ruta  final de la pagina, por lo que recomiendo dejar un nombre como *my-blog* o *profile*... Aunque si aún no lo has decidido, no hay problema, ya que puedes cambiarlo más adelante en las configuración del repositorio.
2. Luego ir a su configuración y en la sección **pages** indicar que rama será la que contendra el contenido de la página.
3. Una vez guardado el cambio, aparecera un enlace con el link de tu página.


### Primeros pasos con Jekyll

1. Primero clona el repositorio en un carpeta local, puede ser en escritorio o donde quieras.
2. Ingresa a la carpeta del repositorio
3. Crea un nuevo proyecto Jekyll con el comando `jekyll new .` este arrojará un error debido a que jekyll espera a que tu carpeta este vacia, pero tenemos un archivo Readme.md, por ello debes ejecutar el comando `jekyll new . --force` el cual creara la estructura de carpetas y archivos del poyecto
4. Ve al archivo **_config.yml** y modifica la url base que definirá tu página, en mi caso:
   - `baseurl: "/my-blog"`
5. Levanta la página localmente con el comando `bundle exec jekyll serve --livereload`
6. Dirigete a *http://127.0.0.1:4000/nombre-de-tu-baseurl/* en tu navegador y veras como la mágia ocurre.


### Como publicar en la web de Github la Página

1. Lo primero es cumplir con el primer paso **Creación de un repositorio en Github**
2.  Ve al archivo **_config.yml** y modifica la url que definiera tu página, en mi caso:
   - `url: "https://fernandonavajas.github.io"`
3. Ve al archivo **Gemfile** y comenta la linea donde se hace uso de la gema jekyll
   - `# gem "jekyll", "~> 4.2.0"`
4. En el mismo archivo **Gemfile** descomenta la linea
   - `gem "github-pages", group: :jekyll_plugins`
5. Ejecuta el comando `bundle update`, luego `bundle install`, para actualizar y instalar las dependencias de la aplicación que hemos comentado
6. recargar el servidor y ve ;).
7. Sube los cambios, espera unos 5 minutos y ve a la direccion donde se publico tu página, en mi caso : *https://fernandonavajas.github.io/my-blog/*


### Como editar tu primer post

1. Como lograste ver en el navegador, si has completado los pasos anteriores, se puede ver un post publicado con la bienvenida de Jekyll. En el se indica que puedes encontrarlo en la aplicación en una carpeta llamada **_posts**, para poder realizar modificaciones sobre ese post, basta con ir a **_post/fecha-welcome-to-jekyll.markdown** y editar el archivo.
2. Si quieres crear tu propio archivo, ya debes imaginar como hacerlo, puedes duplicar el generico **fecha-welcome-to-jekyll.markdown** y borrar su contenido (ojo: la cabecera esta envuelta entre 3 guiones `---` está contiene la informacion del post, como el título, la fecha, la categoria y a que layout pertenece).
3. Ya una vez creado el nuevo post, lo podrás ver en la lista de post de la página levanta localmente.
4. Recomiendo cambiar los datos título, email y descripción ubicadoe en el archivo **_config.yml**, cuando cambiamos algo en la configuración de Jekyll, debemos reiniciar el servidor.
   - `title: Blog`
   - `email: fernandonavajas1@gmail.com`
   - `description: Bienvenido al blog`


### Ponte creativo

Con jekyll se han hecho un montón de páginas muy usadas como:

- [Ruby on Rails][ror]
- [Sketch][sketch]
- [Spotify Developer][spotify_developer]
- [Ionic][ionic]

Intenta darle un ojo a estos sitios y a [otros][otros-sitios] y puede que te animes a crear tu propia página sin mucho esfuerzo.

Tambien dejare la documentación del [QuickStart][jekyll-docs] de Jekyll

[otros-sitios]: https://jekyllrb.com/showcase/
[ionic]: https://ionicframework.com/
[spotify_developer]: https://developer.spotify.com/
[sketch]: https://sketch.com/
[ror]: http://rubyonrails.org/
[jekyll-docs]: https://jekyllrb.com/docs/home