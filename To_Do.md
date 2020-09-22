## Plantillas (templates)
* generar plantillas de estilos (`.dot` en Microsoft Word`) para generar uniformidad en el resultado final, sea en la versión pdf, xml y html.

## Tipografías
* check http://kyleamathews.github.io/typography.js/
* en el caso de grafías (latín, idiomas orientales, lenguas muertas) deben suministrarse los archivos: sea en formato truetype, open type, etc. 
* asimismo, debe especificarse si es del tipo `right to left`, `up to down` (ej.: japanese)

## Gráficos
* chequear este servicio para reducir el tiempo de carga. Tienen un CDN propio. Chequear en esta URL: https://www.cloudimage.io/en/home

## Server
* agregar `robots.txt`. Más información [acá](https://yoast.com/ultimate-guide-robots-txt/#robots-txt-location). Agregar [este archivo ya creado](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/892c4d1e94a9a0d526aa031baac512c7650baffe/robot.txt?at=master).
* agregar `.htaccess`. Más información puede encontrarse [aquí](https://hipertextual.com/archivo/2012/07/archivo-htaccess-apache/)
* agregar `favicon.ico`.
* Pasar el test de íconos a través de los distintos dispositivos _et alia_. URL: https://realfavicongenerator.net/
* ~~Chequear~~ / ~~generar archivo~~ [CNAME](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/ebb5ba07eed0078ac583cfd8e25170832d857228/CNAME?at=master&fileviewer=file-view-default) en el servidor (esta es la última instancia, una vez que esté todo listo para ir _online_). --> hecho
* ~~agregar y configurar este [cron job](https://bitbucket.org/snippets/imhicihu/bed47L/ojs-cron-job)~~ --> hecho
* crear cuenta (gratis) en https://cron-job.org/en/
* chequear este _modus-operandi_: https://github.com/typicode/hotel

## OJS
* ~~actualizar a la última versión estable de OJS~~ --> hecho
* Cómo saber que versión tenemos instalada. Consultar este [snippet](https://bitbucket.org/snippets/imhicihu/6eggK8/verify-with-version-is-installed-on-my)
* Generar _checklist_ que muestre el flujo de trabajo: envío, corrección, publicación de los _papers_. Más información [acá](https://pkp.sfu.ca/wiki/index.php?title=OJS_Workflow:_Stages)

## OJS Backup
* ~~Backup (no hay plugin para la última versión, por ende, hay que hacerlo de manera manual, via FTP o Panel de control)~~
* Más información recabada, ver [`backup.md`](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/eb57ad32778c727442dbf0b3628681697273e36a/Backup.md?at=master&fileviewer=file-view-default)

## OJS Plugins
* ~~discriminar los _plugins_ a instalar~~  ---> Hecho ----> Ver [`plugins.md`](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/17e63fd547d1a2a6bdbac5cfe35cbe4508f15013/Plugins.md?at=master&fileviewer=file-view-default)
* ~~translation of plugins~~ ---> Hecho

## OJS Analíticas
* ~~habilitar el plugin `Google Analytics Plugin`~~ ---> Hecho
* ~~hay que relacionarlo con una cuenta de Gmail, ergo, hay que poseer una cuenta de Gmail~~ ---> Hecho 
* ~~procedimiento para insertar el código de seguimiento de _Google Analytics_ dentro del sitio y/o complemento (léase `plugin`) [acá](https://support.google.com/analytics/answer/1008080?hl=es)~~ ---> Hecho

## OJS Tipografía
* [Webfonts Beginner´s guide](https://design.google/library/choosing-web-fonts-beginners-guide/)  
* enfocarse en el `HTML Markup` y en el esquema `xlm`
![glyphs.png](https://bitbucket.org/repo/rpybXp8/images/3991009943-glyphs.png)
* [Font Testing Page](https://github.com/impallari/Font-Testing-Page/): tests de tipografías en pantalla (kerning, interlineado, etc.)

## OJS Seguridad
* restringir qué tipo de documento puede subirse (léase `.doc`, `.docx`, `.rtf`)
* asociar una cuenta de Gmail para después habilitar `Recaptcha`. Aquí está el [procedimiento](https://www.google.com/recaptcha/admin?hl=es#list) a seguir. **Crucial para evitar spam**
* Restricción en qué tipo de archivos se pueden subir ---> ver [acá](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/6fdb683c746db6179f7cce22e45c74316ab5d737/file_type_restriction.md?at=master&fileviewer=file-view-default).   Solución: habilitar el plugin [`Allowed uploads`](https://github.com/ajnyga/allowedUploads)
* agregar la dirección definitiva del sitio en 
     - [UptimeRobot](https://uptimerobot.com/)
     - [Monitor.Us](http://www.monitis.com/)
     - [Montastic](http://montastic.com/)
     - [BasicState](http://basicstate.com/)

## OJS Legales
* ~~Cookies (Política de cookies). (creación de alerta acerca de las cookies de acuerdo a la legislación de cada país. Ir [aquí](https://cookieconsent.insites.com/download/) para generar el archivo de javascript~~ --> Hecho. Más info [aquí](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/issues/6/workflow-texto-de-las-cookies)
* Política de privacidad (creación del texto legal de acuerdo a nuestro país y de acuerdo a cada país). Ver [`Privacidad.md`](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/d984b71e541d43893651dacec2ca34eb1ea44e41/Privacidad.md?at=master&fileviewer=file-view-default) a modo de ejemplo

## OJS Plantilla
* intimamente relacionado con la generación/conversión automática a formatos `XML` & `html`
* crear plantilla (ej: `.dot` para archivos de Microsoft Word®) conteniendo:
     - título
     - subtítulo 1
     - subtítulo 2
     - subtítulo 3
     - leyenda
     - Bibliografía
* el archivo resultante, copiarlo o transferirlo a este repositorio: https://bitbucket.org/imhicihu/template-of-digital-publication/
* check this jquery --> [Page Scroll Indicator](https://github.com/alssndro/page-scroll-indicator)

## OJS Misceláneas
* Generar mapa del sitio. 
* ~~Primera condición: definir la dirección de internet definitiva (URL)~~ ---> Hecho ∫ Check this commit: https://bitbucket.org/imhicihu/open-journal-system-ojs-project/commits/3dd51705c328b21cfec59dab14709a00610242ce
* Después seguir estos [pasos](https://github.com/pkp/ojs/blob/master/docs/README-SITEMAP)
* Generar estas páginas estáticas:
     - site map
     - status page
     - colophon page
     - cookie policy
     - 404 Page not found (_Página no encontrada_)
     - 503 Service Temporarily Unavailable (_Servicio temporariamente no disponible_)
* Donde dice: `Contacte con su administrador/a del sitio (imhicihu conicet, mail@imhicihu-conicet.gov.ar) para avisarles de esta nueva versión`. **CAMBIAR EL CORREO ELECTRONICO** Esta leyenda se encuentra [acá](http://ojs-imhicihu.experttel.com.ar/index.php/TemasMedievales/management/settings/context)
* todas las imágenes deben tener su correspondiente descripción, uno para semantizar todos los elementos de la página, más aun, mejorar la "calificación" de los buscadores, más aun, para cumplir con las reglas de "Buenas prácticas" (**agregar referencias de ARIA norms**)
* dar soporte a [Citation Style](https://github.com/citation-style-language)
* formato de archivos contemplados: 
```
     [LibreOffice](https://www.documentfoundation.org/) 
     [OpenOffice](http://www.openoffice.org)
     [NeoOffice](http://www.neooffice.org)
```
* Open Typesetting Stack --> para convertir doc a html & xml. Más data [acá](https://pkp.sfu.ca/open-typesetting-stack/)

## PHP Error console log
* check this Stackeroverflow [thread](https://stackoverflow.com/questions/5127838/where-does-php-store-the-error-log-php5-apache-fastcgi-cpanel)

## Del.icio.us migration
* ~~Migrate Del.icio.us gathered links to Evernote~~
* ~~Check this previous~~ [thread](https://bitbucket.org/imhicihu/migration-bookmarks-to-evernote/src/master/Procedure.md)

## Security
* [Domain privacy](https://www.namecheap.com/security/whoisguard/)

## Legal ##
* All trademarks are the property of their respective owners.