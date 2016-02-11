BullSheet Repository
=========================
2016-02-10



A repository where you store the bullsheets.
 
 
 
 
What's a BullSheet repository?
-----------------------


It's a repository used by the [BullSheet](https://github.com/lingtalfi/BullSheet) generator,
which is a php7 generator to create random data to populate your database.

Pull requests are welcome.



Structure of this bullsheets repository
----------------------------------------

Bullsheets are organized by namespace.

This is done so, so that when you use a BullSheetGenerator, you just need to import the whole namespace into your 
local machine, and you can start generating random data right away.

For more information, please refer to the documentation of the [BullSheet planet](https://github.com/lingtalfi/BullSheet).



```
- root/
----- $namespace (your namespace, like ling for instance)
--------- (your bullsheets)
```
 





History Log
------------------
    
- 1.1.0 -- 2016-02-11

    - add ling/lorem 
    
- 1.0.0 -- 2016-02-10

    - initial commit
    
    