<div class="center">
  <h1>Pages</h1>
  <p>An application for precision production of Notebooks.</p>
</div>

## Configuration
```yaml
book:
  coverpage: boolean # true === enabled; Adds 2 front pages cover/contact.
  index: boolean # true === enabled; Adds 4 index pages to front behind cover.
  leftpage: string # set to the filename (without extension) of an include.
  rightpage: string # set to the filename (without extension) of an include.
  diameter: float # controls the .svg spacing for lined/dotgrid pages.
  pagecount: integer # sets the number of left/right pages to add to the output.
```

## Goals

## Why
I made this app in a frenzied few hours on Christmas Eve, 2019. The reason I
made this as an app, instead of doing the graphic design work by hand was due to
the belief that the technologies and learnings I gained from doing it this way
would come in handy for developing the "Future App".

And then I went ahead and made it in Jekyll. So. It cannot do many of the things
I would like it to do, and, frankly, the configurations are such a nightmarishly
contrived thing that I have had great difficulty in refactoring any of the
useful bits out.


## TODO (or things I've noticed wrong)
- Cover Page has a hardcoded image name/location. This would be an ideal target
    for breaking out into a variable, though I'm unsure when.
- Index Pages have no configurable count (ideally this should be based upon the
    number of total pages, however this index page design is kind of
    antiquated//odd anyhow.
- I actually like the cover pages better when they're blank. No gaudy jpg
    compression artifacts, just a blank coloured pages. If this were
    implemented, then I would need to change the contact form to be the 1st page
    front. As it stands, I really don't find it very attention-grabbing in the
    prototype units.
- There is no programmed running of the PDF generation upon any changes being
    made. This all has to be done manually (and that is far from ideal).
