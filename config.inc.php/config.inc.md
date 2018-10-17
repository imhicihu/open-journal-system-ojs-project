# config.inc.php (check this settings)


      ; Enable support for running scheduled tasks
      ; Set this to On if you have set up the scheduled tasks script to
      ; execute periodically
        scheduled_tasks = On (CHANGE TO THIS)
		
	  ; Site time zone
      ; Please refer to lib/pkp/registry/timeZones.xml for a full list of supported
      ; time zones.
      ; I.e.:
      ; <entry key="Americas/Buenos Aires" name="Buenos Aires" /> (CHANGE TO THIS)
      ; time_zone="Buenos Aires"  (CHANGE TO THIS)
      time_zone = "UTC-3"  (CHANGE TO THIS)
	  
      ; Base URL override settings: Entries like the following examples can
      ; be used to override the base URLs used by OJS. If you want to use a
      ; proxy to rewrite URLs to OJS, configure your proxy's URL here.
      ; Syntax: base_url[journal_path] = http://www.myUrl.com
      ; To override URLs that aren't part of a particular journal, use a
      ; journal_path of "index".
      ; Examples:
      ; base_url[index] = http://www.myUrl.com  (VERIFY WITH MARIA LAURA)
      ; base_url[myJournal] = http://www.myUrl.com/myJournal (VERIFY WITH MARIA LAURA)
      ; base_url[myOtherJournal] = http://myOtherJournal.myUrl.com  (VERIFY WITH MARIA LAURA)
      
      ; Allow javascript files to be served through a content delivery network (set to off to use local files)
      enable_cdn = On  (CHANGE TO THIS)  (BOOTSTRAP FOSTER CDN linking, so keep it)