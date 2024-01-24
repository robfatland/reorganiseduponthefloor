# Markdown


## 1. headers


GitHub supports markdown format: When a github file with extension `.md` is opened 
(in a browser I mean) the contents are reflected according to "markdown" formatting protocol.


Common markdown formatting includes ***headers***. The following text:

```
# Major Heading
## Subsection
### Subsubsection
#### Pretty fine grained at this point
##### Very fine grain
```

renders as

# Major Heading
## Subsection
### Subsubsection
#### Pretty fine grained at this point
##### Very fine grain



## 2. The back-tick character 


The back-tick found at keyboard upper left looks like this: \` .
To print this character here I used the backslash *literal* delimiter; so the markdown is **\\\`**  . 


Use: Back-ticks produce fixed-width-font text. This is useful for indicating or quoting `commands` and 
`code`. 


A single back-tick keeps the resulting text inline with the surrounding text. For example this sentence has \`True\` in the markdown which renders inline as `True`. 
Three back-ticks delimit multi-line code blocks:


```
def Bumpkins(n, qi):
    for i in range(n):
        print('oh dear, this is tragic...')
```

Notice that the back-tick is a *verbatim* delimeter. Other delimiters are not respected when they occur 
inside a backtick field. However asterisk delimiters *outside* of backtick delimiters work fine. Compare:
`**asterisks inside**` versus **`asterisks on the outside`**. 


## 3. asterisks


In this text please find single, double, and triple asterisk delimiters. 
\*Single\*. \*\*Double\*\*. \*\*\*Triple\*\*\* produces *Single* **Double** ***Triple***. 


## 4. quotations


A leading `>` character renders text as a quotation. 


> This is useful to offset "special note" offset blocks of text. 


## 5. hyperlinks 


Place the text to appear within square bracks and follow it with no spaces by the link URL 
in parentheses. [This link goes to the Google search page](https://google.com). It
is constructed as `[link text](https://google.com)`. 


Within a document viewed in a browser: Holding the cursor over a link reveals the link address.
Within a page, links to headers are simple: Type a pound sign \# followed by
a header name with spaces replaced by hyphens.
[This link jumps up to the asterisk section](#1.-headers).



## 6. html


HTML can be embedded in a markdown file.


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
