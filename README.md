# PDF-Indexer
A python script to scrape a pdf file and create a word index out of it.

A [word index](https://en.wikipedia.org/wiki/Index_(publishing)#Purpose) is a sorted list of important words in a document, where each word is tagged by the all the page numbers it appears in. For example, in a book about cats, an index might look like this 

Cute 1,2,5,7

Eyes 3,4,5

Paws 2,3,4

Whiskers 5,6,7

The numbers that follow each word is all the page numbers where the word appeared. This helps you find a word quickly.

## How To Use

Use any python installation with the library [pdfplumber](https://github.com/jsvine/pdfplumber) installed. You can do it with 

    pip install pdfplumber
    
as usual.

Invoke the script as follows

    python indexer.py PDF="PATH\TO\PDF\FILE\INCLUDING\EXTENTSION.pdf" TXT="PATH\TO\OUTPUT\FILE\INCLUDING\EXTENSION.txt"

You can also remove the string double qoutations if the file name has no spaces in it.

## Efficiency

The script is somewhat a sloth. It takes about a minute to index a pdf file of about 500 pages on an intel core i7 4th gen dual 2.9 GHz core machine with 8GB RAM and an HDD, running a Windows 8.1 instance. 

I think there is no realistic way to improve it as most of the time appears to be spent in the pdfplumber code. But I will try.  
