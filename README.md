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
 


Create your own bullsheets
------------------------------

A bullsheet is simply a text file, with entries in it, one by line.
For instance, this is the content of a bullsheet for rainbow colors:

```
red
orange
yellow
green
blue
indigo
violet
```

Put that in a .txt file and there you have your bullsheet.


A tool that uses the bullsheets is the [BullSheet planet by lingtalfi](https://github.com/lingtalfi/BullSheet).

If you want to share your bullsheets via this repository, just send a pull request.



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



What lists are in there?
---------------------------

I've added a few lists, but I have my own way of organizing things, so probably the best thing to do is to have a look 
at the [categories](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling).


So far, we can differentiate two types of lists, text lists, and media lists.


### Text lists


- [list of actors](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/actor/given_name)
- [list of adjectives](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/adjective),
        [list of emotional adjectives](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/adjective/emotion/all)
- [list of album titles](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/album_title/wordlab)
- [list of book titles](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/book_title/wordlab/nonfiction)
- [list of charlie sheen sentences](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/comment/sheen),
        you can assemble them randomly to create some fake comments; actually the [LingBullSheetGenerator](https://github.com/lingtalfi/BullSheet)
        has a comment method that does just that.
- [lists of companies](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/company)
- [list of first names](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/first_name/all) and 
        [list of last names](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/last_name/international),
        even a [list of female names](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/last_name/international/female)
        and a [list of male names](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/last_name/international/female)
- [list of email provider](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/free_email_provider_domain/all)
- [list of iso 639-1 lang code](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/iso639-1/all) and 
            [list of iso 639-2 lang code](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/iso639-2/all)
- [list of lorem sentences and words](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/lorem)

- [list of youtube info](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/miscellaneous/youtube_info/10000), 
    each line contains the youtube id, the duration, the title, the thumbnail and the description 

- [list of movie directors](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/movie_director) (male and female)
- [list of movie genres](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/movie_genre/all)
- [list of movie titles](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/movie_title)
- [list of music genres](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/music_genre/all)
- [list of common passwords](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/password/common)
- [list of product names](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/product_name/wordlab)
- [list of american pseudo](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/pseudo/american)
- [list of slogan](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/slogan/wordlab)
- [list of titles](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/title/all)
- [list of top level domains](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/top_level_domain/all)
- [list of tv programs](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/tv_program/wikipedia/all)
- [list of urls](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/url), including
        a [list of real youtube urls](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/url/youtube/10000),
        a [list of fake facebook urls](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/url/facebook/fakeurls),
        a [list of fake twitter urls](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/url/twitter/fakeurls),
        and more...
- [list of website domains](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/website_domain/alexa)
- [list of words](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/word/english), including 
        [lists of words indexed by letters](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/word/english/dwyl/word1)


### Medias lists

- [list of images](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/image/vintage)
- [tiny demo list of mp3](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/mp3/demo)
- [tiny demo list of video](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/video/demo)
 




Resources
------------

Amongst the best resources I've come across for collecting bullsheet repositories data:

- http://www.wordlab.com/archives/
- https://en.wikipedia.org/wiki/Portal:Contents/Lists




History Log
------------------
    
- 1.13.0 -- 2016-02-13

    - add [youtube info list](https://github.com/bullsheet/bullsheets-repo/tree/master/bullsheets/ling/miscellaneous/youtube_info/10000)
    
    
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
    
    