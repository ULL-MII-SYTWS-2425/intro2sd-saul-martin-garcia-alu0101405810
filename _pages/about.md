---
permalink: /about/
title: "Sobre Mí"
excerpt: "Conoce más sobre mí y mi pasión por la tecnología."
---

# 👋 ¡Hola! Soy Saúl

Soy graduado en **{{ site.data.profile.career }}** y actualmente tengo **{{ site.data.profile.age }} años**. Trabajo como **{{ site.data.profile.job_title }}**, donde disfruto creando soluciones eficientes y escalables. Además, estoy cursando un **{{ site.data.profile.current_study }}**, lo que me permite profundizar mis conocimientos y habilidades en el campo.

## 🛠️ Tecnologías y Herramientas

- **Lenguajes de programación**: {% for language in site.data.profile.technologies.languages %}{{ language }}{% unless forloop.last %}, {% endunless %}{% endfor %}
- **Frameworks**: {% for framework in site.data.profile.technologies.frameworks %}{{ framework }}{% unless forloop.last %}, {% endunless %}{% endfor %}
- **Bases de datos**: {% for db in site.data.profile.technologies.databases %}{{ db }}{% unless forloop.last %}, {% endunless %}{% endfor %}
- **Herramientas de desarrollo**: {% for tool in site.data.profile.technologies.tools %}{{ tool }}{% unless forloop.last %}, {% endunless %}{% endfor %}

## 📚 Aprendizaje Continuo

Me apasiona aprender y explorar nuevas tecnologías y tendencias en el desarrollo de software. Si tienes recomendaciones de libros, cursos o tecnologías interesantes, ¡no dudes en compartírmelas!

## 📫 Conéctemos

- **LinkedIn**: [{{ site.data.profile.linkedin.name }}]({{ site.data.profile.linkedin.url }})
- **Correo**: [{{ site.data.profile.contact.email }}](mailto:{{ site.data.profile.contact.email }})

¡Gracias por visitar mi perfil! Estoy emocionado por las oportunidades de colaboración y aprendizaje que puedan surgir.

## Mis Proyectos

{% for proyecto in site.data.proyectos.proyectos %}

<div class="proyecto-card">
  <div class="proyecto-header">
    <h3>{{ proyecto.titulo }}</h3>
    <span class="proyecto-estado {{ proyecto.estado | downcase }}">{{ proyecto.estado }}</span>
  </div>

  <p class="proyecto-descripcion">{{ proyecto.descripcion }}</p>
  
  <div class="proyecto-tecnologias">
    {% for tech in proyecto.tecnologias %}
      <span class="tech-tag">{{ tech }}</span>
    {% endfor %}
  </div>
  
  <div class="proyecto-footer">
    <span class="proyecto-fecha">{{ proyecto.fecha }}</span>
    {% if proyecto.url %}
    <a href="{{ proyecto.url }}" class="proyecto-enlace" target="_blank">
      <i class="fas fa-external-link-alt"></i> Ver Proyecto
    </a>
    {% endif %}
  </div>
</div>
{% endfor %}

## Enlace al despliegue en Netlify

[Despliegue en Netlify](https://intro2sd-saul-martin-garcia-alu010140.netlify.app/)
