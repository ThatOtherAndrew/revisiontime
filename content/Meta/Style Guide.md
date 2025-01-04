*See also: [[Contribution Guide]]*

Revision Time is a collaborative wiki project, and as with all collaborative wiki projects, it's important to have a **style guide** to keep everyone on the same page. This page aims to explain **how to shape what you write**.

> [!example] Examples of good pages
> To get a sense for what's being aimed for, check out the following pages which set a good example:
> 
> - [[Hyperbolic Function]]
> - [[Unit Hyperbola]]

## Narrative
Everybody naturally has a different way in which they write their notes, however there are a few core qualities which should be strived for in writing.

### Make it intuitive!
Most importantly of all, wherever possible, try to **present all ideas as intuitively as you can**. Lead the reader on their own journey of discovery! Play with ideas and explore their implications, connections and elaborations. It's *exceptionally* difficult to do, but if you were to put yourself into the shoes of a new learner, try to **align your writing** as much as possible with **wherever their thought process would naturally lead**.

Ideally, a perfect page would make every section seem like a logical next step following on from the previous step, and should guide the reader enough such that they feel like they could've figured it out for themselves given enough time.

**Memorisation is your worst enemy!**

### Telling a story
Every page, especially its [[#overview]], should **aim to tell a story**. There should be a logical progression of events, such that a reader starting from the top of the page and reading to the bottom should be able to make sense of what's going on at every point. Any assumed knowledge or understanding should preferably be explicitly mentioned and [[#Links|linked to]].

If two ideas are introduced in a page such that understanding idea A is necessary or helpful for understanding idea B, then idea A should be presented earlier in the page.

### Tone of writing
This isn't a formal thesis! Feel free to talk casually, address the reader, use slang, or otherwise play about in your text. It really helps to add a personal touch to it!

Just don't use informality as an excuse to get sloppy with your spelling, grammar or formatting please - if you can't tell apart *you're* and *your* then [you're outta luck and your grammar sucks](https://youtu.be/-FdKPEA17m4).

### Humour
Humour is great! Unlike Wikipedia, we can afford to be a little silly here. Not only does it spice up what may be otherwise quite dull notes, but it actually helps improve information retention as well - a reader is more likely to remember something that they found mildly amusing.

Try to aim to inject a little humour into your writing wherever appropriate, if you don't already! However, it should go without saying that you should be cautious around sensitive topics and avoid targeted insults.

![[nerd.png|What you look like reading this|200]]

Insulting the reader doesn't count as being targeted, though.

## Structure and layout

Standardising the way that information is laid out is important, as it ensures a consistent experience for readers and minimises the friction when trying to find information. I have drawn some inspiration from Wikipedia for structuring information, but in a much looser manner; you'll notice this page is much shorter than the behemoth that is the [Wikipedia Manual of Style](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style).

### Pages
Every page should correspond to a **single topic or concept** which is **not too narrow in scope**. It's hard to pin down exactly what this means, but a good rule of thumb is that you should be able to give a **reasonable amount of information** beyond just a simple definition, and **identify subtopics** covered under the broader page topic.

> [!tip] Adapting existing notes
> One significant challenge with contributing any existing class or lecture notes is this organisation of notes by topic or concept.
> 
> If you can split your notes apart and re-collate them in such a manner that they're grouped by topic and [[#Telling a story|follow a continuous narrative]], it'd be greatly appreciated and would save me a lot of work!

Page names should be concise, singular, and given in [Title Case](https://en.wikipedia.org/wiki/Title_case). In the case that a concept has multiple names or terms to describe it, choose the more common term and mention the other term(s) in the [[#overview]]. If a page name is ambiguous or too generic, additional context can be provided in parentheses, but this should be a last resort.

Pages are sorted in alphabetical order under folders corresponding to the module in which the concept is first introduced. For example, a page on complex numbers would reside at `MT1002/Complex Number`.

In the case that a page's topic is very broad, it should aim to provide a comprehensive introduction to the topic and link to other pages on more specific concepts.

> [!success] Examples of good page names
> - **Complex Number**
> - **Sonata Form**
> - **Deep Vein Thrombosis**
> - **Integer Overflow**
> - **Electron Transport Chain**
> - **Stream (Java)**

> [!failure] Examples of bad page names
> - **Complex Numbers** (shouldn't be plural)
> - **sonata form** (should be in Title Case)
> - **DVT** (abbreviation is too vague)
> - **Integer Overflow and Underflow** (too verbose)
> - **Symptoms of DVT** (too narrow/specific)
> - **Stream** (too ambiguous)

### Overview
A page's overview is the **section at the top of the page**, before the first heading. The overview should provide an introduction into the topic of the page, with information about the intuition or logical steps to get to the concept if relevant.

**All pages must have an overview section.**

A good overview should be sufficient on its own to give the reader a surface-level understanding of **what the concept is** and **where it comes from**, with the rest of the page being made up of [[#headings]] detailing and exploring various more specific aspects of the concept.

For an example of a good overview, see the start of the [[Complex Number]] page.

### Headings
After the [[#overview]], a page should usually contain a number of **headings**. Unlike page titles, headings should be in **Sentence case** (i.e. just the first letter capitalised) and can be singular or plural, whichever reads more naturally.

Top-level headings in a page should be **h2 headings**, notated as `## two hashes` in Markdown. Headings can be **nested heirarchically**, with `h3` headings falling under `h2`, `h4` under `h3` and so on. This is used to generate the *On This Page* navigation outline in the sidebar.

Unlike the overview, headings are not mandatory in a page, as it's not necessary if all relevant information can be covered reasonably in one continuous stream of prose in the overview. However, for the vast majority of pages, having headings is strongly recommended.

## Content

### Links
Adding links between [[#pages]] and [[#headings]] helps to draw connections between related topics and concepts, which aids the reader's understanding. Whenever a topic covered by a different page or heading is referenced in a page, there should be at least one link provided to it.

This site's content is written using [Obsidian](https://obsidian.md), which supports [both Wikilink and Markdown notation](https://help.obsidian.md/Linking+notes+and+files/Internal+links). Don't worry though - when contributing, you can label your links however you wish or just omit it altogether and I'll use my own judgement to decide how to add links.

However, try to avoid falling into the trap of **overlinking**! If you mention a concept 10 times in a page or section, you don't need to link every single mention of it - just the first one should usually be enough.

### Images
All image embeds can include a **caption** underneath them, which has its content taken from the image's [alt text](https://webaim.org/techniques/alttext/) and defaults to the filename. (Yes, this somewhat sucks for accessibility, but unfortunately this is currently a technical limitation.)

![[640px-Utah_teapot_simple_2.png|Here is an example of an image caption. (For the curious, this is the Utah teapot!)|400]]

If you have a particularly witty or valuable caption to submit alongside an image in your contribution, just write it in below the image and I'll handle the caption formatting.

### Other media
There are many other types of rich content which can be embedded in a page, including but not limited to YouTube videos, Twitter/X tweets, audio files, or even other entire websites. More technically, **any static HTML content** can be embedded. This is used for the interactive animated Desmos graphs in [[Hyperbolic Function#Parametric plots of cos/cosh, sin/sinh]], for example.

If you're contributing, just a link to whatever content you wish to embed should suffice, and I'll handle the embedding. If you're feeling really fancy, you can directly include the HTML code as well.
