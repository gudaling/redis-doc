

Save the DB in background. The OK code is immediately returned.
Redis forks, the parent continues to server the clients, the child
saves the DB on disk then exit. A client my be able to check if the
operation succeeded using the [LASTSAVE][1] command.

@return

[Status code reply][2]



[1]: /p/redis/wiki/LastsaveCommand
[2]: /p/redis/wiki/ReplyTypes