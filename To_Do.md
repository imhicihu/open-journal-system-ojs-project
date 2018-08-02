## Server
* agregar `robot.txt`. Más información [acá](https://yoast.com/ultimate-guide-robots-txt/#robots-txt-location)
* agregar `.htaccess`.
* agregar `favicon.ico`.
* Pasar el test de íconos a través de los distintos dispositivos _et alia_. URL: https://realfavicongenerator.net/
* Chequear / generar archivo `CNAME` en el servidor (esta es la última instancia, una vez que esté todo listo para ir _online_).

## OJS
* ~~actualizar a la última versión estable de OJS~~ --> hecho
* Cómo saber que versión tenemos instalada. Consultar este [snippet](https://bitbucket.org/snippets/imhicihu/6eggK8/verify-with-version-is-installed-on-my)
* Generar _checklist_ que muestre el flujo de trabajo: envío, corrección, publicación de los _papers_. Más información [acá](https://pkp.sfu.ca/wiki/index.php?title=OJS_Workflow:_Stages)

## OJS Backup
* ~~Backup (no hay plugin para la última versión, por ende, hay que hacerlo de manera manual, via FTP o Panel de control)~~
* Más información recabada, ver [`backup.md`](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/eb57ad32778c727442dbf0b3628681697273e36a/Backup.md?at=master&fileviewer=file-view-default)

## OJS Plugins
* ~~discriminar los _plugins_ a instalar~~  ---> Hecho ----> Ver [`plugins.md`](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/17e63fd547d1a2a6bdbac5cfe35cbe4508f15013/Plugins.md?at=master&fileviewer=file-view-default)

## OJS Analíticas
* ~~habilitar el plugin `Google Analytics Plugin`.~~
* hay que relacionarlo con una cuenta de Gmail

## OJS Tipografía
* [Webfonts Beginner´s guide](https://design.google/library/choosing-web-fonts-beginners-guide/)  
* enfocarse en el `HTML Markup` y en el esquema `xlm`
* [Font Testing Page](https://github.com/impallari/Font-Testing-Page/): tests de tipografías en pantalla (kerning, interlineado, etc.)

## OJS Seguridad
* restringir qué tipo de documento puede subirse (léase `.doc`, `.docx`, `.rtf`)
* Restricción en qué tipo de archivos se pueden subir ---> ver [acá](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/6fdb683c746db6179f7cce22e45c74316ab5d737/file_type_restriction.md?at=master&fileviewer=file-view-default).   Solución: habilitar el plugin [`Allowed uploads`](https://github.com/ajnyga/allowedUploads)
* agregar la dirección definitiva del sitio en 
     - [UptimeRobot](https://uptimerobot.com/); 
     - [Monitor.Us](http://www.monitis.com/); 
     - [Montastic](http://montastic.com/);  
     - [BasicState](http://basicstate.com/)

## OJS Legales
* ~~Cookies (Política de cookies). (creación de alerta acerca de las cookies de acuerdo a la legislación de cada país. Ir [aquí](https://cookieconsent.insites.com/download/) para generar el archivo de javascript~~ --> Hecho. Más info [aquí](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/issues/6/workflow-texto-de-las-cookies)
* Política de privacidad (creación del texto legal de acuerdo a nuestro país y de acuerdo a cada país). 

## OJS Misceláneas
* Generar mapa del sitio. Primera condición: definir la dirección de internet definitiva (URL). Después seguir estos [pasos](https://github.com/pkp/ojs/blob/master/docs/README-SITEMAP)
* Generar estas páginas estáticas:
     - 404 (página no encontrada)
* Donde dice: `Contacte con su administrador/a del sitio (imhicihu conicet, mail@imhicihu-conicet.gov.ar) para avisarles de esta nueva versión`. **CAMBIAR EL CORREO ELECTRONICO** Esta leyenda se encuentra [acá](http://ojs-imhicihu.experttel.com.ar/index.php/TemasMedievales/management/settings/context)
* todas las imágenes deben tener su correspondiente descripción, uno para semantizar todos los elementos de la página, más aun, mejorar la "calificación" de los buscadores, más aun, para cumplir con las reglas de "Buenas prácticas" (**agregar referencias de ARIA norms**)
* dar soporte a [Citation Style](https://github.com/citation-style-language)
* formato de archivos contemplados: 
```
     LibreOffice 
     [OpenOffice](http://www.openoffice.org)
     [NeoOffice](http://www.neooffice.org)
```
