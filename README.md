md2post
=======

## Synopsis
Just a script for myself aiming at automatic formating code blocks in markdown files
which can be recognized by [jekyll][1].

## The problem

Normal markdown parser identifies _code blocks_ with the starting spaces/tabs of the line.
But [liquid][2] tag `{% hightlight lang %}` won't swallow the first spaces/tabs and identifis
*code blocks* only with the highlight tag.

So if the code blocks is original written this way:

    {% highlight c %}
    
        int main() {
            return 0;
        }
    
    {% endhighlight %}

We will get html like this

        int main() {
            return 0;
        }

## What the script do

- Transform blog articles written at ease into [jekyll][1] blog format
  - add blog metadata at the beginning
  - use current time for default blog time
  - fix code blocks' spaces/tabs at front
- Specify output and input directory

[1]: http://jekyllrb.com/ "jekyll"
[2]: https://github.com/Shopify/liquid "liquid"
