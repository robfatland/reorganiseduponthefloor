$e^{i \pi} + 1 = 0, \ give \ or \ take...$


Please place some version of these notes; as you like; someplace stable. I treat GitHub as my 
"someplace stable" these days. Regardless of whether my laptop falls into a volcano on the sea floor: 
GitHub abides. 


I am writing these notes in the order they occur to me; so this is based on ***improvised pragmatism***.
This first part began as an enumeration but quickly devolves into a story.


> Another version of this material is in a Jupyter notebook in my **`ocean`** repo but it is a 
> bit hard to find. Chapter 5 I believe.


# Markdown


## 1. Intro


GitHub supports markdown format: When a github file with extension `.md` is opened in Chrome
(say) the view reflects the rules of "markdown" as a formatting protocol. Commonly repos
have a "default" markdown file called `README.md`. 


You have the option to create a repo under your user account 
called **`howto`** which contains your version of these notes and so on; maybe it saves 
you some look-up time. Documentation repos might be entirely markdown.


What can markdown do? Well it supports several different types of formatting.


Common markdown formatting includes ***headers***:


# Major Heading
## Subsection
### Subsubsection
#### Pretty fine grained at this point
##### Very fine grain


Next there is...


## 2. The back-tick character 


This is very useful: The back-tick usually found at keyboard upper left: \` .
Of course to print this character here I used 
the backslash *literal* delimiter; so what is in the markdown file is **\\\`**  . 


Use: Back-ticks create blocks of fixed-width font text, as in an older-style
computer terminal. This is useful for indicating or quoting `commands` and 
`computer code`. 


A single back-tick is used as a delimiter for 
code that remains inline with surrounding text. For example this sentence has a `True` in it. 


Use three back-ticks to delimit multi-line code blocks


```
def Bumpkins(n, iq):
    for i in range(n):
        print('oh dear, this is tragic...')
```

Notice that the back-tick is a *verbatim* delimeter. Other delimiters are not respected when they occur 
inside back-ticks. 
On the other hand, asterisk delimiters *outside* of backtick delimiters work great. 
`**asterisks inside**` versus **`asterisks on the outside`**. 


Speaking of...


## 3. asterisks


In this text please find single, double, and triple asterisk delimiters. 
*Single*. **Double**. ***Triple***. How about do ****four asterisks in a row**** do anything different? 


## 4. quotations


A leading `>` character renders text as a quotation. 


> This is useful to offset "special note" blocks of text. 


## 6. hyperlinks 


Place the text to appear within square bracks and follow it with no spaces by the link URL 
in parentheses. [This link goes to the Google search page](https://google.com). It
is constructed as `[link text](https://google.com)`. 


Within a document, cursor hover over headings reveals link addresses.
You can copy and paste those into the (hyperlink) following a \[link name\].
For within a page, links to headers are simpler: Just a pound sign \# followed by
the header name; with spaces replaced by hyphens.
[This one goes up to the back-tick section](#2-the-back-tick-character), for
example. The link string here is `#2-the-back-tick-character`.



## 6. html


HTML can be embedded in a markdown file. This is useful, for example, to embed an image 
in a markdown page. More detail is out of scope at the moment. 


## 7. wandering off into the story


Now I turn to the last topic of this segment, a digression. The practical matter of `git` is 
deferred to a subsequent page.


Some years ago -- never mind how long precisely -- one of our possible heroes 
was asked to write a book. 
He was working as an assistant professor at a small college in Pasadena at the time; and he took a 
close look at the idea and upped
the ante in reply: "Yes, but wait! My idea is a more ambitious and a better book... in 12 chapters."
Whereupon
he embarked on the expanded project which in turn expanded into a treatise on computer science,
and that work has occupied him to this day, some 60 years later. He appears to 
have done some other work as well
in the mean time. For example he gives interesting lectures each December.
(These may be found on YouTube.)


The history of this book, which I shall refer to using the title acronym TAOCP, is beyond the 
scope of these notes. But it is 
by all accounts a remarkable book, or books, six volumes so far. I have not read 
it as I have not needed it. 
But since I'm discovering it right now I shall check out a copy and we can take a look. It 
concerns algorithms, particularly 
computer algorithms. Back to our story. 


Some years went by from that 1962 starting point; and as technical books are often periodically 
revised, Volume 2 went through
this process in 1976. So it was that our subject received the proofs for TAOCP Volume 2; 
which had been 
typeset in a new manner. 


As an aside you might look up 'Tao'. It seems poetically appropriate
and for Professor Knuth I suspect any found poetry is not 
accidental. I offer as evidence the version numbering system used for
the software described below.
Ah, and it seems I have neglected to properly introduce his name.


Enter stage left: Professor Donald Ervin Knuth. Just one anecdote from his biography: It is not common, 
upon an individual's completing their bachelor's degree, for the
faculty of their institution to conclude that they should also be awarded a master's degree. 


Anyway the proofs for the second edition were found to be wanting. 
So Professor Knuth did what anyone would do upon receiving proofs that suffered from deficient 
typesetting. He designed and wrote his own typesetting system, ensuring it would 
be universally available for anyone's use at no cost. This system he named TeX. It went through
many revisions from 1978 to 1989 when it was 'officially' released; but it was in
serious academic use when I started college in 1982.


This system called TeX has proved to be quite successful: 
Academics and publishing companies and many
other adopters have learned and adopted
it and have created thousands of books and hundreds of thousands of
articles that are a joy to behold, surpassing *readable* to often achieve *beautiful*. 
Forty years and counting, decades more to come. 


I do not use TeX directly. To write my graduate thesis I became moderately fluent in
LaTeX; a content-oriented system that uses TeX for document layout. 
I think
of LaTeX (correctly or incorrectly) as a human-friendly wrapper around TeX. Anyway
by moderate fluency I mean...


$$
x \ = \ \sqrt{1 + 2\sqrt{1 + 3\sqrt{1 + 4\sqrt{1 + 5\sqrt{1 + 6\sqrt{\cdots}}}}}}
$$

...is easy enough in LaTeX syntax. The trick is to have some time on hand
to get it just so.
Whereas
footnotes and page headers and diagrams and tables and things of that sort would 
take me some digging to set up proper. The point is LaTeX is good for all that stuff,
where TeX is bit harder to learn and use.



With that, I'll continue in 
[this document](https://github.com/robfatland/reorganiseduponthefloor/edit/main/git/bash_and_git.md)
on what little I retain about `bash` and `git`. 
