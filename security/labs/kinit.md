# Add Kerberos principal for user
> sudo kadmin.local  
> kadmin.local: addprinc daacn@ARNREICH.COM  
  
# Get Kerberos Ticket
> sudo su daacn  
> kinit  
> Password for daacn@ARNREICH.COM: ...   
>   
> klist
```
Ticket cache: FILE:/tmp/krb5cc_793
Default principal: daacn@ARNREICH.COM

Valid starting       Expires              Service principal
11/17/2016 08:32:17  11/18/2016 08:32:17  krbtgt/ARNREICH.COM@ARNREICH.COM
        renew until 11/24/2016 08:32:17
```