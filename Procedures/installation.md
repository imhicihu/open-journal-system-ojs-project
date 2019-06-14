# Procedures
## System
* Download OJS from [here](https://pkp.sfu.ca/ojs/ojs_download/)
* System requeriments (recommended). Your server will need:
	- PHP >= 7.0
	- MySQL/MariaDB 4.1 or later or PostgreSQL 9.1.5 or later
	- Apache >= 1.3.2x or >= 2.0.4x or Microsoft IIS 6
* Operating system: 
	- Any OS: Linux, BSD, Solaris, Mac OS X, Windows
## Installation
* Download from Extract the OJS archive to the desired location in your web documents directory
* Make the following files and directories (and their contents) writeable:
	- `config.inc.php` (_optional_ -- if not writable you will be prompted to manually overwrite this file during installation)
	- `public`
	- `cache`
	- `cache/t_cache`
	- `cache/t_config`
	- `cache/t_compile`
	- `cache/_db`
* Create a subdirectory that will host your pdfs, jpeg, etc. Protect it under a rule inside the `.htaccess` file
* Open a web browser to `http://yourdomain.com/path/to/ojs/` and follow the on-screen installation instructions
* Verify `config.inc.php` for additional configuration settings
* Verify your server API PHP. If OJS is already installed, log in as Site Administrator, click `System Information`, and at the bottom of the page, click `Extended PHP Information`. Find the line that says `Server API`. Depending on which API you are using (`mod_php/SAPI` or `CGI/FastCGI`), permissions should be set as follow: 
	- mod_php/SAPI: In this configuration, all PHP scripts on the system typically execute as the same user (usually Apache’s “nobody” or “www-data” accounts). Be warned that this may be insecure on a shared host. The `files_dir` (configured in `config.inc.php`), the cache directory, the public directory, and all contents and subdirectories must be writable and readable by the web server user. The `config.inc.php` configuration file must be readable by the web server user
	- CGI/FastCGI: PHP scripts will typically run under your user account (though server configurations may vary). This can be a well-secured configuration. The `files_dir` (configured in `config.inc.php`), the cache directory, the public directory, and all contents and subdirectories must be writable and readable by this user account. The `config.inc.php` configuration file must be readable by this account.
* Across time, it will be warned about updates. Apply accordingly
* Check `docs` directory: there contains configuration, installation or upgrade questions


