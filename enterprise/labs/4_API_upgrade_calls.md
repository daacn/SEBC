## Latest API Version
> http://ec2-54-167-85-32.compute-1.amazonaws.com:7180/api/version  
> v14  
  
## Current CM Version:
> http://ec2-54-167-85-32.compute-1.amazonaws.com:7180/api/v14/cm/version  
```JSON
{  
  "version": "5.9.0",  
  "buildUser": "jenkins",  
  "buildTimestamp": "20161006-1801",  
  "gitHash": "898a5e032c080e18833dfc58180761f6ef2ea351",  
  "snapshot": false  
}
```
  
## CM Users:
> http://ec2-54-167-85-32.compute-1.amazonaws.com:7180/api/v14/users  
```JSON
{  
  "items": [  
    {  
      "name": "admin",  
      "roles": [  
        "ROLE_ADMIN"  
      ]  
    },  
    {  
      "name": "minotaur",  
      "roles": [  
        "ROLE_CONFIGURATOR"  
      ]  
    }  
  ]  
}  
```