# LOGS

We use the follow snipet to match regex

```
[LOG ENTRY] [ERROR] The system is unstable
[LOG ENTRY] [WARN] The system may be down
[LOG ENTRY] [LOG] Everything is OK
[LOG ENTRY] [LOG] [user:@beco] Logged in
[LOG ENTRY] [LOG] [user:@beco] Clicked here
[LOG ENTRY] [LOG] [user:@beco] Rated the app
[LOG ENTRY] [LOG] [user:@beco] Logged out
```
If we wanna find all WARN logs, we can use the follow:
-```^\[LOG.*\[WARN\].*$```
This regex can be read as follows
Find a start of line with``` \[``` remember escape the [ character, It's reserved
Then
Find ```LOG``` word followed by anything ```-*```
Until it finds ```[WARN]``` and followed for anything until end of line.

## Some util regex to logs

### Find Http methods
- ```^.*((GET)|(POST)|(PUT)|(DELETE)).*$```

### Find Ip addresses
- ```(\d{1,3}\.){3,3}(\d{1,3})```

### Find dates with format DD/MM/YYYY
- ```^.*(\d{1,2}\/\w+\/\d{4,4}).*$```