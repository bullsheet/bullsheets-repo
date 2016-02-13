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

For more information, please refer to the documentation of tallhe [BullSheet planet](https://github.com/lingtalfi/BullSheet).



```
- root/
----- $namespace (your namespace, like ling for instance)
--------- (your bullsheets)
```
 



How much lines should contain a file?
--------------------

Short answer: 50000 lines or less, on unix (not tested on windows).


I'm very angry when I wait, waiting 1 second is just something I can't do.

Here are my observations about the relationship between the number of lines of a data file,
and the time that the BullSheetGenerator.getPureData method takes to pick one line,
using an unix machine (algorithm is optimized for those machines).


- 50 000 is almost (I can see that it's not really) instantaneous, I would use that inside a 1000 iterations foreach loop
- 100 000 is noticeable but fast (I'm ok with it)
- 150 000 is unacceptable for me (but it's less than one second)






Resources
------------

Amongst the best resources I've come across for collecting bullsheet repositories data:

- http://www.wordlab.com/archives/
- https://en.wikipedia.org/wiki/Portal:Contents/Lists




History Log
------------------
    
- 1.12.0 -- 2016-02-13

    - add video
    - add mp3
        
- 1.11.0 -- 2016-02-13

    - add comment
    
- 1.10.0 -- 2016-02-13

    - add tv_program
      
    
- 1.9.0 -- 2016-02-13

    - add movie_title/wikipedia    
        
- 1.8.0 -- 2016-02-12

    - add url/facebook
    - add url/twitter
    - add url/linkedin
    - add url/google_plus 
        
- 1.7.0 -- 2016-02-12

    - reorganize title

- 1.6.0 -- 2016-02-12

    - add company
    - add album_title
    - add movie_title
    - add book_title
    - add product_name
    - add title
    - add slogan 
	
- 1.5.0 -- 2016-02-12

    - add movie_genre
	- add movie_director
	- add adjectives
	- add more in word 
    
- 1.4.0 -- 2016-02-11

    - add password 
        
- 1.3.0 -- 2016-02-11

    - add music_genre 
        
- 1.2.0 -- 2016-02-11

    - add word 
    - add url 
    - add images 
        
- 1.1.0 -- 2016-02-11

    - add ling/lorem 
    
- 1.0.0 -- 2016-02-10

    - initial commit
    
    