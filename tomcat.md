# Tomcat

* How to configure logging in tomcat.log for a Tomcat-based web application: Put

  `   org.apache.level = ALL`

  in `logging.properties`. This creates huge amounts of log data, but you can narrow it down to HTTP connections, for example:

  `   org.apache.coyote.level = FINE`
  
* [Very good article on HTTPS configuration in Tomcat](https://blog.eveoh.nl/2014/02/tls-ssl-ciphers-pfs-tomcat/)
