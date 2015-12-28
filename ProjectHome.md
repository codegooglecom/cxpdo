This class extends the PDO object to provide DB abstraction - a simple way to query different types of databases without needing to change your code.

PDO:
> PDO provides a **data-access** abstraction layer, which means that, regardless of which database you're using, you use the same functions to issue queries and fetch data. PDO does not provide a database  abstraction; it doesn't rewrite SQL or emulate missing features. You should use a full-blown abstraction layer if you need that facility. - http://php.net/manual/en/intro.pdo.php

However PDO does not cover DB **query-abstraction** - for that you have to use some huge class like [ADOdb](http://adodb.sourceforge.net/) or [PEAR:DB](http://pear.php.net/package/DB). Which of course will slow your site to a crawl if you are using shared hosting.

This class fills this gap and provides DB **query-abstraction** for common functions like SELECT, REPLACE, INSERT, UPDATE, and DELETE queries. The actual PDO object is not changed in anyway - each of these functions still returns a PDO Statement Object.

The total package size is only 18kb! And that is with LOTS of comments explaining the code! It is the missing link for people who love the DATA abstraction PDO provides but also need QUERY abstraction.

Currently it only works on SQLite2-3 and MySQL. However because it is built for the SQL langauge - it will be supper simple to add PostgreSQL or MSSQL support as well (copy mysql class and change 3-5 functions). I just don't have a copy of either DB up and running to test it.