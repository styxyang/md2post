md2post
=======

Just a script for myself aiming at automatic formating code blocks in markdown files.

The problem:

Normal markdown parser identifies _code blocks_ with the starting spaces/tabs of the line.
But `liquid` tag `{% hightlight lang %}` won't swallow the first spaces/tabs and identifis
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
