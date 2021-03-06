# __Integrar Facebook Messenger a Nuestra Web__ 
![Messenger](https://scontent.flim19-1.fna.fbcdn.net/v/t39.8562-6/120009688_325579128711709_1736249742330805861_n.png?_nc_cat=1&ccb=2&_nc_sid=6825c5&_nc_ohc=ozHS44QT50YAX99Vpa2&_nc_ht=scontent.flim19-1.fna&oh=c58408793cc13d0bee6f5522d5c97587&oe=5FEB007D)
## [Business Facebook](https://business.facebook.com/)
1. Iniciar sesión en Facebook
2. Seleccionar el FanPage
2. Ir a Información
3. Copiar el identificador de la página
4. Ir a configuración (Plataforma de Messenger)
5. Agregar el url de la web en la sección dominios admitidos
##  [Developers Facebook](https://developers.facebook.com/)
1. Iniciar sesión en Developers Facebook
2. Agregar una APP
3. En el Dashboard copiamos el identificador de la APP

### Luego nos dirigimos a la [Documentación](https://developers.facebook.com/docs/)
---
1. HERRAMIENTAS PARA EMPRESAS
---
    1.1. Messenger Platform
    1.2. Descubrimiento
    1.3. Plugin de chat de cliente
    1.4. Incluir el plugin en la página web
```html
<div class="fb-customerchat" page_id="<PAGE_ID>"></div>
```
---
2. SDK PARA JAVASCRIPT
---
    2.1. Inicio rápido
    2.2. Configuración básica
```javascript
<script>
  window.fbAsyncInit = function() {
    FB.init({
      appId            : 'your-app-id',
      autoLogAppEvents : true,
      xfbml            : true,
      version          : 'v3.2'
    });
  };

  (function(d, s, id){
     var js, fjs = d.getElementsByTagName(s)[0];
     if (d.getElementById(id)) {return;}
     js = d.createElement(s); js.id = id;
     js.src = "https://connect.facebook.net/es_LA/sdk/xfbml.customerchat.js";
     fjs.parentNode.insertBefore(js, fjs);
   }(document, 'script', 'facebook-jssdk'));
</script>
```
Recuerda que debemos cambiar el idioma por defecto que es __`en_US`__ por __`es_LA`__.
<br>Por último, agregamos el código antes de cerrar la etiqueta __`</body>`__ en nuestra web.
<br>Elaborado por [Genaro Hernández](https://genarohernandez.pro)
