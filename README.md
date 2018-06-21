# pg\_lib

# Administration:
* Remove public schemas:
  https://www.postgresql.org/docs/current/static/ddl-schemas.html#DDL-SCHEMAS-PATTERNS
* user == role. Also, users are just roles with LOGIN privilege.
* SIGTERM: Smart shutdown: https://www.postgresql.org/docs/9.6/static/server-shutdown.html
* Don't use /tmp for UNIX domain sockets. Create private directories and configure PG to use them.
  * For TCP connections, use SSL only. Client need to check certificates of server:
    https://www.postgresql.org/docs/current/static/preventing-server-spoofing.html

# Introductions:
* PG screencasts: Free: https://www.pgcasts.com/
* Better Database Migrations in Postgres: https://news.ycombinator.com/item?id=15235221
* PG Exercises: https://pgexercises.com
* Secure/lockdown PG:
  * https://www.upguard.com/articles/10-ways-to-bolster-postgresql-security
  * https://www.trustwave.com/Resources/SpiderLabs-Blog/Helping-to-Secure-your-PostgreSQL-Database/
  * Users & roles: https://blog.2ndquadrant.com/auditing-users-and-roles-in-postgresql/

* RLS for web apps: https://blog.2ndquadrant.com/application-users-vs-row-level-security/


# Videos:
* http://www.youtube.com/watch?v=s-BvKkVSyTA
* https://www.youtube.com/watch?v=20FNSWhatq4
* https://www.youtube.com/watch?v=_wU2dglywAU
