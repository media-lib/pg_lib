
Security Notes:
==============

* trust = never use
* specific users, even for superusers. Don't use
  'postgres' user. Use LDAP instead.
* set specific listen_address

* granular permissions: tedious, hardork.

* don't login as 'web'. Have a specific role.

* Postgres stores passwords in mD5 (crackable).
  Use LDAP.

* lock roles to application servers: db migration, web app role, etc

* Require SSL or else MitM attacks, esp. in cloud environments.

* encrypt certain columns. Use TEXT or bytea.

* pgcrypto: Do not use because logging functionailty defeats
  purpose. use app. layer encryption.

* Secure logs:
  * rsyslog to keep logs secured off the box.
  * set logging to min. 0 to log psql and pgadmin4 activity.
  * encrypt the logs if storing in clouds.

Videos:
* http://www.youtube.com/watch?v=s-BvKkVSyTA
* https://www.youtube.com/watch?v=20FNSWhatq4
* https://www.youtube.com/watch?v=_wU2dglywAU
