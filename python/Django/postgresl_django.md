## to fix django key already exists 

sqlsequencereset¶
django-admin sqlsequencereset app_label [app_label ...]¶
Prints the SQL statements for resetting sequences for the given app name(s).

Sequences are indexes used by some database engines to track the next available number for automatically incremented fields.

Use this command to generate SQL which will fix cases where a sequence is out of sync with its automatically incremented field data.

--database DATABASE¶
Specifies the database for which to print the SQL. Defaults to default.



## or postgresl solution 

SELECT setval('users_id_seq', (SELECT MAX(id) from "users"));
