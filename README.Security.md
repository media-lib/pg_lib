
Security Notes:
==============

* "$HOME/.pgpass": permissions should be u=rw (0600) or less

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

* Behind a firewall.

* pg_hba.conf:
  * Use md5, not Trust
  * Bottom: host all all all reject
  * host: localhost only. Don't use '\*', '0.0.0.0', '::' as these are wildcard values for any address, IPv4 addresses, or 
  IPv6 addresses.

* Owners == small superuser that can grant itself other privileges. Create a read user and don't use the owner user/role for application connections.

* Check for unnecesary privileges:
  * "Testing Roles": https://blog.2ndquadrant.com/auditing-users-and-roles-in-postgresql/


