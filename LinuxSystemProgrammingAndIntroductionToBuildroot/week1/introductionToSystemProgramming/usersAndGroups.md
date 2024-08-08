# Linux Users and Groups
- user logs in with a username and password (Authentication)
- each user is associated with a User ID (uid)
    - each process is associated with the UID of the user runnig the process
    - /etc/passwd maps username uids
- UID 0 is the root user
    - can do almost anything on the system
- each user belongs to one or more groups, with correspondign Group ID (gid)
    - /etc/groups maps group names to gids
