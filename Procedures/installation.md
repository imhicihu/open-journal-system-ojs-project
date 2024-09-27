### Procedures
#### System
* Download OJS from [here](https://pkp.sfu.ca/ojs/ojs_download/)
* System requirements (recommended). Your server will need:
	- PHP >= 7.0
	- MySQL/MariaDB 4.1 or later or PostgreSQL 9.1.5 or later
	- Apache >= 1.3.2x or >= 2.0.4x or Microsoft IIS 6
* Operating system: 
	- Any OS: Linux, BSD, Solaris, Mac OS X, Windows
#### Installation
* Download from extract the OJS archive to the desired location in your web documents directory
* Make the following files and directories (and their contents) writeable:
	- `config.inc.php` (_optional_, if not writable you will be prompted to manually overwrite this file during installation)
	- `public`
	- `cache`
	- `cache/t_cache`
	- `cache/t_config`
	- `cache/t_compile`
	- `cache/_db`
* Create a subdirectory that will host your pdfs, jpeg, etc. Protect it under a rule inside the `.htaccess` file
* Open a web browser to `http://yourdomain.com/path/to/ojs/` and follow the on-screen installation instructions
* Verify `config.inc.php` for additional configuration settings
![config.php.jpg](/images/4241243587-config-php.jpg)
* Verify your server API PHP. If OJS is already installed, log in as Site Administrator, click `System Information`, and at the bottom of the page, click `Extended PHP Information`. Find the line that says `Server API`. Depending on which API you are using (`mod_php/SAPI` or `CGI/FastCGI`), permissions should be set as follow: 
	- mod_php/SAPI: In this configuration, all PHP scripts on the system typically execute as the same user (usually Apache’s “nobody” or “www-data” accounts). Be warned that this may be insecure on a shared host. The `files_dir` (configured in `config.inc.php`), the cache directory, the public directory, and all contents and subdirectories must be writable and readable by the web server user. The `config.inc.php` configuration file must be readable by the web server user
	- CGI/FastCGI: PHP scripts will typically run under your user account (though server configurations may vary). This can be a well-secured configuration. The `files_dir` (configured in `config.inc.php`), the cache directory, the public directory, and all contents and subdirectories must be writable and readable by this user account. The `config.inc.php` configuration file must be readable by this account.
* Schedule tasks (such as automatic sending of reminder notification emails): enable support for using scheduled tasks, edit your `config.inc.php` and set the `scheduled_tasks` setting to `On`. On Unix operating systems, this can be done by adding a simple cron task:

```# crontab -e www
0 * * * *	php /path/to/ojs/tools/runScheduledTasks.php
```

* check your `file_type_restriction.ini`
![configini.png](/images/3968091645-configini.png)
* `PHP Safe Mode` is not a recommended configuration and may not function properly
* Across time, it will be warned about updates. Apply accordingly
* Check `docs` directory: there it contains configuration, installation or upgrade questions
* To add support for other languages, the following sets of XML files must be localized and placed in an appropriately named directory (using ISO locale 
codes, e.g. `fr_FR`, is recommended):
	- `locale/en_US`
	- `lib/pkp/locale/en_US`
	- `docs/manual/en`
	- `registry/locale/en_US`
	- `plugins/[plugin category]/[plugin name]/locale`, where applicable
* New locales must also be added to the file `registry/locales.xml`. Edit accordingly
* Verify character encoding (preferred `utf-8` format). In a way, we’re storing utf8 data in a utf8 database. Therefore, run these command from the terminal
![code.png](/images/3542055665-carbon.png)
* We are ensuring that the OJS `config.inc.php` settings match the data and `db` settings
* Clear it off comments your css file

#### Configuration
* Browse to the `Settings` > `Websites` > `Plugins` > `Plugin Gallery` page in your Open Journal Systems website setup.
* Enable this plugins:
     * [Backup](https://github.com/asmecher/backup)
     * [iThenticate](https://github.com/asmecher/plagiarism)
     * [QuickSubmit](https://github.com/pkp/quickSubmit)
     * [Allowed Uploads](https://github.com/ajnyga/allowedUploads)
     * [Custom Header](https://github.com/asmecher/customHeader/)
     * [backup](https://github.com/asmecher/backup)
     * Google Analytics
     * DOI
     * [StaticPages](https://github.com/pkp/staticPages)
     * [Shariff plugin](https://github.com/ojsde/shariff)
     * [JATS Template Plugin](https://github.com/asmecher/jatsTemplate/)
* Install a font (preferred) that support non-western glyphs and ligatures. More data can be found [here](/typography/fonts.md)

#### Maintenance
* Verify your webserver error log
* Verify your file permissions
* Check your memory limit on your `PHP` settings. It’s normally set at `8mb` by default, but OJS need at least `16mb` set to run properly. You can find a `memory_limit` configuration directive in your server’s `php.ini` config file.
* Check this [thread](https://bitbucket.org/imhicihu/open-journal-system-ojs-project/src/master/Error_PHP_Console_log.md) about error logs
* Follow this good practices about [backup](Backup.md)

