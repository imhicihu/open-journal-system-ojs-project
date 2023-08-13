### Procedures
#### via *command line*: 
- If you have the *CLI* version of PHP installed (e.g., `/usr/bin/php`), you can upgrade the database as follows:
- Edit `config.inc.php` and change `installed = On` to `installed = Off`
- Run the following command from the OJS directory (not including the $): $ `php tools/upgrade.php upgrade`
- Re-edit `config.inc.php` and change `installed = Off` back to `installed = On`
#### via web:
- Edit `config.inc.php` and change `installed = On` to `installed = Off`
- Open a web browser to your installed OJS site; you should be redirected to the installation and upgrade page
- Select the `Upgrade` link and follow the on-screen instructions
- Re-edit `config.inc.php` and change `installed = Off` back to `installed = On`
