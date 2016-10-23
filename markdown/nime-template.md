1998

See <http://www.acm.org/about/class/1998/> to obtain categories and
subject descriptors for classifying this paper. An example follows:

H.5.5 \[Information Interfaces and Presentation\] Sound and Music
Computing, H.5.2 \[Information Interfaces and Presentation\] User
Interfaces—Haptic I/O, I.2.9 \[Artificial Intelligence\]
Robotics—Propelling mechanisms.

**The new requirements for classifying the papers at the time of
submission are detailed. It is strongly recommended that authors view
the submission form prior to starting to write the paper. See the file
`ScientificProgramSubmissionFormPreview.pdf` for a preview. (Do *not*
create a dummy submission to view the submission form.)**

Introduction
============

The *proceedings* are the records of a conference. ACM seeks to give
these conference by-products a uniform, high-quality appearance. To do
this, ACM has some rigid requirements for the format of the proceedings
documents: there is a specified format (balanced double columns), a
specified set of fonts (Arial or Helvetica and Times Roman) in certain
specified sizes (for instance, 9 point for body copy).

The good news is, with only a handful of manual settings,[^1] the
LaTeX document class file handles all of this for you.

The remainder of this document is concerned with showing, in the context
of an “actual” document, the LaTeX commands specifically available for
denoting the structure of a proceedings paper, rather than with giving
rigorous descriptions or explanations of such commands.

The <span>Body</span> of The Paper
==================================

Typically, the body of a paper is organized into a hierarchical
structure, with numbered or unnumbered headings for sections,
subsections, sub-subsections, and even smaller sections. The command
`’134section` that precedes this paragraph is part of such a
hierarchy.[^2] LaTeX handles the numbering and placement of these
headings for you, when you use the appropriate heading commands around
the titles of the headings. If you want a sub-subsection or smaller part
to be unnumbered in your output, simply append an asterisk to the
command name. Examples of both numbered and unnumbered headings will
appear throughout the balance of this sample document.

Because the entire article is contained in the **document** environment,
you can indicate the start of a new paragraph with a blank line in your
input file; that is why this sentence forms a separate paragraph.

Type Changes and <span>Special</span> Characters
------------------------------------------------

We have already seen several typeface changes in this sample. You can
indicate italicized words or phrases in your text with the command
`’134textit`; emboldening with the command `’134textbf` and
typewriter-style (for instance, for computer code) with `’134texttt`.
But remember, you do not have to indicate typestyle changes when such
changes are part of the *structural* elements of your article; for
instance, the heading of this subsection will be in a sans serif[^3]
typeface, but that is handled by the document class file. Take care with
the use of[^4] the curly braces in typeface changes; they mark the
beginning and end of the text that is to be in the different typeface.

You can use whatever symbols, accented characters, or non-English
characters you need anywhere in your document; you can find a complete
list of what is available in the *LaTeXUser’s Guide* [@Lamport:LaTeX].

Tables
------

Because tables cannot be split across pages, the best placement for them
is typically the top of the page nearest their initial cite. To ensure
this proper “floating” placement of tables, use the environment
**table** to enclose the table’s contents and the table caption. The
contents of the table itself must go in the **tabular** environment, to
be aligned properly in rows and columns, with the desired horizontal and
vertical rules. Again, detailed instructions on **tabular** material is
found in the *LaTeX User’s Guide*.

Immediately following this sentence is the point at which
Table \[tab:frequency\] is included in the input file; compare the
placement of the table here with the table in the printed dvi output of
this document.

To get correct numbering of tables, please use the **label** command
inside the **table** environment and a corresponding **ref** in the
text.

   Non-English or Math    Frequency   Comments
  --------------------- ------------- -------------------
            Ø            1 in 1,000   For Swedish names
          $\pi$            1 in 5     Common in math
           \$              4 in 5     Used in business
       $\Psi^2_1$        1 in 40,000  Unexplained usage

  : Frequency of Special Characters

\[tab:frequency\]

To set a wider table, which takes up the whole width of the page’s live
area, use the environment **table\*** to enclose the table’s contents
and the table caption. As with a single-column table, this wide table
will “float" to a location deemed more desirable. Immediately following
this sentence is the point at which Table 2 is included in the input
file; again, it is instructive to compare the placement of the table
here with the table in the printed dvi output of this document.

\[htbp\]

          Command          A Number  Comments
  ----------------------- ---------- --------------------
     `’134alignauthor`       100     Author alignment
   `’134numberofauthors`     200     Author enumeration
        `’134table`          300     For tables
       `’134table*`          400     For wider tables

Figures
-------

Like tables, figures cannot be split across pages; the best placement
for them is typically the top or the bottom of the page nearest their
initial cite. To ensure this proper “floating” placement of figures, use
the environment **figure** to enclose the figure and its caption.
Optionally, for small figures that you want to place inline with the
text, you can use the **htbp** options to **figure** to see whether
there is space for placing it inline with the text.

This sample document contains examples of **.pdf**
(Figure \[fig:BlockDiagram1\]) and **.jpg** files to be displayable with
LaTeX. More details on each of these is found in the *Author’s Guide*.

![A sample image in PDF format.<span
data-label="fig:BlockDiagram1"></span>](BlockDiagram1){width="1\columnwidth"}

As was the case with tables, you may want a figure that spans two
columns (Figure  \[fig:BlockDiagram2\]). To do this, and still to ensure
proper “floating” placement of tables, use the environment **figure\***
to enclose the figure and its caption. And don’t forget to end the
environment with <span>figure\*</span>, not <span>figure</span>!

\[htbp\] ![image](BlockDiagram2){width="100.00000%"}

Math Equations
--------------

You may want to display math equations in three distinct styles: inline,
numbered or non-numbered display. Each of the three are discussed in the
next sections.

### Inline (In-text) Equations

A formula that appears in the running text is called an inline or
in-text formula. It is produced by the **math** environment, which can
be invoked with the usual `’134begin. . .’134end` construction or with
the short form `$. . .$`. You can use any of the symbols and structures,
from $\alpha$ to $\omega$, available in LaTeX[@Lamport:LaTeX]; this
section will simply show a few examples of in-text equations in context.
Notice how this equation: $\lim_{n\rightarrow \infty}x=0$, set here in
in-line math style, looks slightly different when set in display style.
(See next section).

### Display Equations

A numbered display equation – one set off by vertical space from the
text and centered horizontally – is produced by the **equation**
environment. An unnumbered display equation is produced by the
**displaymath** environment.

Again, in either environment, you can use any of the symbols and
structures available in LaTeX; this section will just give a couple of
examples of display equations in context. First, consider the equation,
shown as an inline equation above: $$\lim_{n\rightarrow \infty}x=0$$
Notice how it is formatted somewhat differently in the **displaymath**
environment. Now, we’ll enter an unnumbered equation:
$$\sum_{i=0}^{\infty} x + 1$$ and follow it with another numbered
equation: $$\sum_{i=0}^{\infty}x_i=\int_{0}^{\pi+2} f$$ just to
demonstrate LaTeX’s able handling of numbering.

Theorem-like Constructs
-----------------------

Other common constructs that may occur in your article are the forms for
logical constructs like theorems, axioms, corollaries and proofs. There
are two forms, one produced by the command `’134newtheorem` and the
other by the command `’134newdef`; perhaps the clearest and easiest way
to distinguish them is to compare the two in the output of this sample
document:

This uses the **theorem** environment, created by the`’134newtheorem`
command:

Let $f$ be continuous on $[a,b]$. If $G$ is an antiderivative for $f$ on
$[a,b]$, then $$\int^b_af(t)dt = G(b) - G(a).$$

The other uses the **definition** environment, created by the
`’134newdef` command:

If $z$ is irrational, then by $e^z$ we mean the unique number which has
logarithm $z$: $${\log e^z = z}$$

Two lists of constructs that use one of these forms is given in the
*Author’s Guidelines*.

There is one other similar construct environment, which is already set
up for you; i.e. you must *not* use a `’134newdef` command to create it:
the **proof** environment. Here is a example of its use:

Suppose on the contrary there exists a real number $L$ such that
$$\lim_{x\rightarrow\infty} \frac{f(x)}{g(x)} = L.$$ Then
$$l=\lim_{x\rightarrow c} f(x)
= \lim_{x\rightarrow c}
\left[ g{x} \cdot \frac{f(x)}{g(x)} \right ]
= \lim_{x\rightarrow c} g(x) \cdot \lim_{x\rightarrow c}
\frac{f(x)}{g(x)} = 0,$$ which contradicts our assumption that
$l\neq 0$.

Complete rules about using these environments and using the two
different creation commands are in the *Author’s Guide*; please consult
it for more detailed instructions. If you need to use another construct,
not listed therein, which you want to have the same formatting as the
Theorem or the Definition [@salas:calculus] shown above, use the
`’134newtheorem` or the `’134newdef` command, respectively, to create
it.

A <span>Caveat</span> for the TeX Expert
----------------------------------------

Because you have just been given permission to use the `’134newdef`
command to create a new form, you might think you can use TeX’s
`’134def` to create a new command: *Please refrain from doing this!*
Remember that your LaTeX source code is primarily intended to create
camera-ready copy, but may be converted to other forms – e.g. HTML. If
you inadvertently omit some or all of the `’134def`s recompilation will
be, to say the least, problematic.

Citations
---------

Citations to articles
[@bowman:reasoning; @clark:pct; @braams:babel; @herlihy:methodology],
conference proceedings [@clark:pct] or books
[@salas:calculus; @Lamport:LaTeX] listed in the Bibliography section of
your article will occur throughout the text of your article. You should
use BibTeX to automatically produce this bibliography; you simply need
to insert one of several citation commands with a key of the item cited
in the proper location in the `.tex` file [@Lamport:LaTeX]. The key is a
short reference you invent to uniquely identify each work; in this
sample document, the key is the first author’s surname and a word from
the title. This identifying key is included with each item in the `.bib`
file for your article.

The details of the construction of the `.bib` file are beyond the scope
of this sample document, but more information can be found in the
*Author’s Guide*, and exhaustive details in the *LaTeX User’s Guide*
[@Lamport:LaTeX] and in various online source.[^5]

This article shows only the plainest form of the citation command, using
`’134cite`. This is what is stipulated in the SIGS style specifications.
No other citation format is endorsed or supported.

Links
-----

Links to URLs can be included using the `’134url` command. This will
generate a clickable link like this: <http://www.nime2013.org>.

Conclusions
===========

This paragraph will end the body of this sample document. Remember that
you might still have Acknowledgments or Appendices; brief samples of
these follow. There is still the Bibliography to deal with; and we will
make a disclaimer about that here: with the exception of the reference
to the LaTeX book, the citations in this paper are to articles which
have nothing to do with the present subject and are used as examples
only.

Acknowledgments
===============

This section is optional; it is a location for you to acknowledge
grants, funding, editing assistance and what have you. In the present
case, for example, the authors would like to thank Gerald Murray of ACM
for his help in codifying this *Author’s Guide* and the **.cls** and
**.tex** files that it describes.

Headings in Appendices
======================

The rules about hierarchical headings discussed above for the body of
the article are different in the appendices. In the **appendix**
environment, the command **section** is used to indicate the start of
each Appendix, with alphabetic order designation (i.e. the first is A,
the second B, etc.) and a title (if you include one). So, if you need
hierarchical structure *within* an Appendix, start with **subsection**
as the highest level. Here is an outline of the body of this document in
Appendix-appropriate form:

Introduction
------------

The Body of the Paper
---------------------

### Type Changes and Special Characters

### Math Equations

#### Inline (In-text) Equations

#### Display Equations

### Citations

### Tables

### Figures

### Theorem-like Constructs

### A Caveat for the TeX Expert {#a-caveat-for-the-texexpert-1 .unnumbered}

Conclusions
-----------

Acknowledgments
---------------

Additional Authors
------------------

This section is inserted by LaTeX; you do not insert it. You just add
the names and information in the `’134additionalauthors` command at the
start of the document.

References
----------

Generated by bibtex from your  .bib file. Run latex, then bibtex, then
latex twice (to resolve references) to create the  .bbl file. Insert
that  .bbl file into the .tex source file and comment out the command
`’134thebibliography`.

More Help for the Hardy
=======================

The sig-alternate.cls file itself is chock-full of succinct and helpful
comments. If you consider yourself a moderately experienced to expert
user of LaTeX, you may find reading it useful but please remember not to
change it.

[^1]: Two of these, the <span>`’134 numberofauthors`</span> and
    <span>`’134 alignauthor`</span> commands, you have already used;
    another, <span>`’134 balancecolumns`</span>, will be used in your
    very last run of LaTeX to ensure balanced column heights on the last
    page.

[^2]: This is the second footnote. It starts a series of three footnotes
    that add nothing informational, but just give an idea of how
    footnotes work and look. It is a wordy one, just so you see how a
    longish one plays out.

[^3]: A third footnote, here. Let’s make this a rather short one to see
    how it looks.

[^4]: A fourth, and last, footnote.

[^5]: See e.g. <http://www.bibtex.org/>.
