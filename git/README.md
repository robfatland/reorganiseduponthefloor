$e^{i \pi} + 1 = 0, \ give \, or \. take...$


Please place some version of these notes; as you like; someplace stable. I treat GitHub as my 
"someplace stable" these days. Regardless of whether my laptop falls into a volcano on the floor of the ocean: GitHub abides. 


I am writing these notes in the order they occur to me; so this is based on ***improvised pragmatism***.
This first part began as an enumeration but quickly devolves into a story.


## 1. Markdown


GitHub supports markdown format: When a github file with extension `.md` is opened in Chrome
(say) the view reflects the rules of "markdown" as a formatting protocol. This includes a "default" 
file at the top of the repo called `README.md`. You might create a repo under your user account 
called **`howto`** which contains your notes for important / commonly used procedures. 
That repo need not have any Python or java or whatever; it might be entirely markdown. 


Common markdown formatting includes....


# Major Heading
## Subsection
### Subsubsection
#### Pretty fine grained at this point
##### Very fine grain


## 2. The back-tick character 


This is very important (keyboard upper left: `) A single back-tick is used as a delimiter for 
code that remains inline with surrounding text. For example this sentence has a `True` in it. 


Use three back-ticks to delimit multi-line code blocks


```
def Bumpkins(n, iq):
    for i in range(n):
        print('oh dear, this is tragic...')
```

Notice that the back-tick is a *verbatim* delimeter. Other delimiters are not respected when they occur inside back-ticks. 
On the other hand, asterisk delimiters *outside* of backtick delimiters work great. `**this**` versus **`this`**. 


## 3. asterisks


In this text please find single, double, and triple asterisk delimiters. 
*Single*. **Double**. ***Triple***. Do ****four in a row**** do anything different? 



HTML can be embedded in a markdown file. This is useful, for example, if you would like to embed an image in a markdown page. But this is beyond scope for this email. 

Now we turn to the last topic of this email, which is a digression. The practical matter of git is deferred to a subsequent email.

Some years ago -- never mind how long precisely -- one of our heroes to whom you have not yet been introduced was asked to write a book. He was working as an assistant professor at a small college in Pasadena California at the time; and he took it on himself to reply "Yes, but wait! Let me write a more ambitious and a better book." Upon receiving approval he embarked on the project which has occupied him to this day, some 60 years. The history of this book, which I shall abbreviate using its acronym TAOCP, is beyond the scope of this email. But it is by all accounts a remarkable book, in multiple volumes. I have not read it but I rather think I ought to, now that I am exploring this topic. It concerns algorithms, particularly computer algorithms.

Now some years went by and books are often periodically revised. So it was that our subject received the proof sheets for the second edition of Volume 2 of his TAOCP book. 

As an aside you might look up a thumbnail sketch of 'Tao' since it is rather poetically appropriate in this context. And when Professor Knuth is involved, one suspects that any poetry is not by accident. 

So enter stage left one Donald Ervin Knuth. 

Anyway the proofs were considered inferior compared to how things looked in the first edition. So Prof Knuth did what anyone else would do upon receiving proofs plagues by inferior quality typesetting. 
