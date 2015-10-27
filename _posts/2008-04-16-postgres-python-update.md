---
ID: 738
post_title: Postgres Python update..
author: David
post_date: 2008-04-16 18:32:59
post_excerpt: ""
layout: post
permalink: >
  https://davidawindham.com/postgres-python-update/
published: true
---
Python 2.5.2, Postgres 8.3.1, and Django .96
<img src="http://davidawindham.com/images/django97.png" alt="django python" />
<img src="http://davidawindham.com/images/python98.png" alt="python 2.5" />
<img src="http://davidawindham.com/images/django99.png" alt="django python" />
i've been playing around again with python today... i went ahead and upgraded my <a href="http://www.postgresql.org/">postgresql</a> and <a href="http://www.python.org/">python</a> on my machine... nothing too tough, although i spent an hour going in loops until i realize that the some of the python scripts were not in usr/local/bin as i always say.. if i'd only read the actual install.txt file before i started hacking away..
<img src="http://davidawindham.com/images/django_admin.png" alt="django admin.py" />
i also ran into a problem with psycopg.. <a href="http://tringtring.wordpress.com/tag/python-django-postgres-psycopg2-mac-os-x/">tring tring</a> suggested using macports for ver2.. as configuration can be <a href="http://code.djangoproject.com/wiki/SetupOnTiger">tricky</a> modifying the config for <a href="http://initd.org/pub/software/psycopg/">psycopg</a>(PostgreSQL database adapter)
psycopg is different from the other database adapter because it was designed
for heavily multi-threaded applications that create and destroy lots of
cursors and make a conspicuous number of concurrent INSERTs or UPDATEs.
Every open Python connection keeps a pool of real (UNIX or TCP/IP) connections
to the database. Every time a new cursor is created, a new connection does not
need to be opened; instead one of the unused connections from the pool is
used. That makes psycopg very fast in typical client-server applications that
create a servicing thread every time a client request arrives. (**this has something to do with news organizations using <a href="http://www.ellingtoncms.com/">ellington</a>) or Django/Python setup with postgres.
Common problems while building psycopg:
1/ if your compiler does not find some postgres headers try copying all the
headers from the postgres _source_ distribution to a single place. Also,
if building postgresql from source, make sure to install all headers by
the "make install-all-headers" target.
2/ if you have the same problem with mx.DateTime, try using the source
directory again; the install script does not copy all the headers, same
way as postgres install procedure does.
3/ under MacOS X you may need to run the runlib program on the posgres
installed libraries before trying to compile psycopg. Also, if you
get compilation errors there is a change your python was not compiled
correctly and psycopg is grabbing the wrong compile-time options from
python's Makefile. try setting the OPT and LDFLAG environment variables
to something usefull...
i can confirm that <a href="http://code.djangoproject.com/wiki/SetupOnTiger">this works</a>. 