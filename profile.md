---
layout: profile
title: Perfil
show_sidebar: true
---

Hola, me llamo Fernando Navajas y Soy un programador, actualmente este sitio es para pruebas


### 1. Ir a otros sitios de la pagina
[Link para ir a los post](/my-blog{% link index.markdown%})

### 2 .renderizar contenido dependiendo de una variable
{% if page.show_sidebar %}
  <div class="sidebar">
    sidebar content
  </div>
{% endif %}

### 3. Bloque de codigo ruby
{% highlight ruby %}
def foo
  puts 'Esto es un bloque de codigos'
end
{% endhighlight %}
