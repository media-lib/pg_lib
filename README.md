# pg_lib


* PG screencasts: Free: https://www.pgcasts.com/
* Better Database Migrations in Postgres: https://news.ycombinator.com/item?id=15235221
* PG Exercises: https://pgexercises.com
* Secure/lockdown PG:
  * https://www.upguard.com/articles/10-ways-to-bolster-postgresql-security
  * https://www.trustwave.com/Resources/SpiderLabs-Blog/Helping-to-Secure-your-PostgreSQL-Database/
  * Users & roles: https://blog.2ndquadrant.com/auditing-users-and-roles-in-postgresql/
  
* RLS for web apps: https://blog.2ndquadrant.com/application-users-vs-row-level-security/
  
# Notes:
* user == role. Also, users are just roles with LOGIN privilege.

# Checklist:
* Behind a firewall.
* pg_hba.conf:
  * Use md5, not Trust
  * Bottom: host all all all reject
  * host: localhost only. Don't use '\*', '0.0.0.0', '::' as these are wildcard values for any address, IPv4 addresses, or IPv6 addresses.
* Owners == small superuser that can grant itself other privileges. Create a read user and don't use the owner user/role for application connections.

* Check for unnecesary privileges:
  * "Testing Roles": https://blog.2ndquadrant.com/auditing-users-and-roles-in-postgresql/
