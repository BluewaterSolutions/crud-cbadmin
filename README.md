# crud-cbadmin

[![Master Branch Build Status](https://img.shields.io/travis/BluewaterSolutions/crud-cbadmin/master.svg?style=flat-square&label=master)](https://travis-ci.org/BluewaterSolutions/crud-cbadmin)

## Sample Usage ##
Please note that this is a work in progress and is currently just a tool to get things started.



Create a new module:
```
contentbox create module directory=modules/contentbox/modules_user name=quickCRUD
cd modules/contentbox/modules_user/quickCRUD
```


Even though we're not using ORM for this, i'm using the orm-entity to create the database structure as well as scaffold out everything else.

```
coldbox create orm-entity entityName=Property properties=first,last,email,address1,address2,city,state,zip table=bluweb__properties primaryKey=id generator=native
```


The above will create a model `models/Property.cfc` that can be deleted after everything has been initialized.


This will read that object and scaffold out the DAO models as well as the views:
```
contentbox create crud-cbadmin entity=models.Property pluralName=Properties moduleName=quickCRUD table=bluweb__properties
```




this can be accessed via: http://yoursite/cbadmin/module/quickCRUD/Properties/index

```

                                       
                                                  $7                        
                                                  $$$                         
                                                 .$$$$                        
                                                 :$$$$.                       
                                                 $$$$$                        
                                               .$$$$$$.                       
                                               $$$$$$$..,                     
                                              $$$$$$+  .$                     
                                             $$$$$=    .Z$                    
                                           .$$$$       .$$Z                   
                                         $$$.$$$$$$$$$$$$$+ . ..             
                                      ..$$$$$$$$$$$$$$7~,......,:+$$I         
                                    .$$$$7.  .                                
888      888                      .+$...              888                                      
888      888                     ..                   888                                      
888      888                                          888                                      
88888b.  888 888  888  .d88b.  888  888  888  8888b.  888888 .d88b.  888d888                   
888 "88b 888 888  888 d8P  Y8b 888  888  888     "88b 888   d8P  Y8b 888P"                     
888  888 888 888  888 88888888 888  888  888 .d888888 888   88888888 888                       
888 d88P 888 Y88b 888 Y8b.     Y88b 888 d88P 888  888 Y88b. Y8b.     888                       
88888P"  888  "Y88888  "Y8888   "Y8888888P"  "Y888888  "Y888 "Y8888  888 

             .dP"Y8  dP"Yb  88     88   88 888888 88  dP"Yb  88b 88 .dP"Y8 
             `Ybo." dP   Yb 88     88   88   88   88 dP   Yb 88Yb88 `Ybo." 
             o.`Y8b Yb   dP 88  .o Y8   8P   88   88 Yb   dP 88 Y88 o.`Y8b 
             8bodP'  YbodP  88ood8 `YbodP'   88   88  YbodP  88  Y8 8bodP' 

```

