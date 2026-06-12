---
layout: post
title: Como construi este blog desde cero, en 15 minutos
date: 2026-06-11T22:50:00.000-04:00
category: Tech
excerpt: "El proceso completo de crear un sitio web personal: dominio, hosting,
  diseño, Git y CMS. Todo paso a paso."
---
## De la idea al sitio publicado

Este sitio nació en una tarde. Lo que parecía complejo resultó ser un proceso ordenado con las herramientas correctas. Acá documento todo lo que hice para que quede registrado y pueda repetirlo o mejorarlo en el futuro.

## 1. El dominio

Compré **canessa.blog** en [Porkbun](https://porkbun.com). Elegí Porkbun por su precio competitivo y su interfaz simple. El dominio `.blog` fue una decisión consciente — describe exactamente lo que es este espacio.

## 2. El hosting

Elegí **Netlify** como plataforma de hosting por tres razones: es gratuito para sitios estáticos, incluye SSL automático y se conecta directamente con GitHub para publicar cambios automáticamente.

## 3. Conectar el dominio

En Porkbun configuré los nameservers de Netlify:

- dns1.p07.nsone.net
- dns2.p07.nsone.net
- dns3.p07.nsone.net
- dns4.p07.nsone.net

La propagación DNS tomó menos de 30 minutos.

## 4. El diseño

El sitio fue construido en HTML y CSS puro — sin frameworks ni librerías pesadas. La paleta de colores es Pantone neutro elegante:

- **Blanc** #F5F3EF — fondos
- **Pearl** #E8E4DC — secciones secundarias
- **Silver** #C9C5BC — fondo principal
- **Stone** #8C887F — textos secundarios
- **Charcoal** #3A3835 — texto principal
- **Caviar** #1C1B19 — títulos

Las tipografías son **Playfair Display** para títulos y **Inter** para el cuerpo. El efecto parallax en el hero fue implementado con JavaScript puro usando el evento `scroll`.

## 5. GitHub y el flujo de publicación

Creé un repositorio en GitHub llamado `canessa-blog` y lo conecté con Netlify. El flujo de trabajo quedó así:

1. Edito en **VS Code**
2. Hago commit desde el panel de Source Control
3. Push con un clic
4. **Netlify publica automáticamente** en segundos

Nunca más necesito la terminal para publicar cambios.

## 6. Decap CMS

Para poder escribir entradas de blog sin tocar código instalé **Decap CMS**. El proceso fue:

1. Activar **Netlify Identity** en la configuración del sitio
2. Crear la carpeta `admin/` con dos archivos: `index.html` y `config.yml`
3. Configurar las colecciones en el YAML
4. Agregar el widget de Netlify Identity al `index.html`
5. Invitarme como usuario y crear contraseña

Ahora puedo escribir desde `canessa.blog/admin` con un panel visual, sin abrir VS Code.

## Próximos pasos

- Favicon y meta tags SEO
- Open Graph para redes sociales
- Google Analytics
- Formulario de contacto con Netlify Forms
- Modo oscuro
- Newsletter

Este sitio es un proyecto vivo. Seguirá creciendo.
