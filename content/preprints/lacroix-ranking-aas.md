+++
title = "b2b lacroix flavor ranking as a service"
date = 2026-09-08
+++

the actual ranking lives at [ymiuraaa.github.io/lacroix](https://ymiuraaa.github.io/lacroix), a separate zola project ([source](https://github.com/ymiuraaa/lacroix)) styled as a 1:1 clone of [prof. david fouhey's ranking](https://cs.nyu.edu/~fouhey/fun/lacroix/). comic sans, weird cursor, all of it. you are now reading the "making of" featurette. there is no dvd. this is the whole bonus feature.

![sneak-peak](/img/lacroix/lacroix-sneakpeak.png)

## flavors are just markdown, the layout is a css trick

no custom data structures. no frontmatter arrays. just vibes, and markdown. a flavor entry is exactly this:

```markdown
![flavor name](images/flavor-name.png)
**flavor name**:
a short review of the flavor.
```

grouped under `## ⭐⭐⭐⭐⭐` style headings, because apparently sparkling water deserved a five-tier ranking system. the template doesn't loop over anything. it just hands `section.content | safe` to the page and walks away. zola sorts it out anyway, which feels like it shouldn't work, but does.

the actual layout comes from one css selector:

```css
p:has(> img) {
    display: inline-block;
    width: 670px;
    text-align: left;
}
```

that's it. that's the whole template. i want to tell you something more technically impressive happened here, but no. css did all the work while i stood nearby, sipping passionfruit flavor lacroix and taking credit.

## turning a random photo into a matching flavor image

grabbing a can photo off the internet and making it match the others (background gone, cropped tight, exact same size) is handled by a script i named `pewpew`. i would like to say the name reflects some deep architectural philosophy. it does not. you run it like this:

```bash
./pewpew static/images/new-flavor.jpg
```

and it flood-fills the background to transparent from the corner, crops to whatever's left, resizes it to a fixed size, and saves a png next to the original. no manual cropping, no fighting with an image editor at 1am questioning your choices. drop the output path into the markdown and you're done.

* you feel weirdly at peace with css selectors now.
