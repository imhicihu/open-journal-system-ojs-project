## Forum
* https://forum.pkp.sfu.ca/t/back-up-of-the-site/37657/2
* https://pkp.sfu.ca/ojs/docs/userguide/2.3.1/systemAdministrationBackup.html

# config.inc.php (check this settings)

      ; Enable support for running scheduled tasks
      ; Set this to On if you have set up the scheduled tasks script to
      ; execute periodically
        scheduled_tasks = Off
		
	  ; Site time zone
      ; Please refer to lib/pkp/registry/timeZones.xml for a full list of supported
      ; time zones.
      ; I.e.:
      ; <entry key="Americas/Buenos Aires" name="Buenos Aires" />
      ; time_zone="Buenos Aires"
      time_zone = "UTC-3"
	  
	  
	  
	  