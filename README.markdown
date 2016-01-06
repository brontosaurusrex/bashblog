# README - how to make a simple markdown blog from cli

## why
* server & client side independent
* open to change
* content is separated from the platform

## a start
    cd
    cd source
    mkdir log
    cd log

## some scripts

**new**

    touch "$(date +"%y%m%d_%H%M%S")_$1.md"
    
usage: `./new postTitle` (should generate empty file named like `141202_221747_postTitle.md`) 

## download some css

    wget http://jasonm23.github.io/markdown-css-themes/foghorn.css
    mv foghorn.css some.css

## some html headers and footers and dividers

**header**

    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="UTF-8">
    <title>my really simple cli log</title>
    <link rel='stylesheet' href="some.css">
    </head>
    <body>
    <h1>~ blog ~</h1>

**footer**

    <br><br>
    (c) brontosaurusrex 2014
    <br>
    </body>
    </html>
    
## make

**make** (simple, not sure if that is the correct way to change order)

    #!/bin/bash

    cat header

    for file in $(find *.md | sort -r)
    do

        cat divider
        pandoc "$file"

    done

    cat footer
    
usage: `./make > blog.htm`
note: fails with whitespaces 

**makecomplex** (pagination) 

    #!/bin/bash
    
    n=5                   # number of files per command line; adjust to taste
    
    readarray -t posts < <(printf %s\\n *.md | sort -r)
    
    for ((i=0; i < "${#posts[@]}"; i+=n)); do
    
            echo "$i.htm ------------------------"
    
            echo "head"
            # each post
            for b in "${posts[@]:i:n}"; do
                echo "---divider---"
                echo "$b" 
            done
            echo "foot"
            echo
            
           # cat "${posts[@]:i:n}"
            
    done




    


## thinkering
* index.htm should be the last N posts = home page
* others could be 1.htm, 2.htm, 3.htm, where 100.htm is just a bit older than index.htm

    
## search your blog from cli
grep OR
    grep -i -E --color 'line|code|who' *.md

## problems

* no search engine

