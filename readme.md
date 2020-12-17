 # CSS Notes (randmom and on course "making sense of the border box model" by Morten Rand-Hendriksen on linkedin learning)

- Box model layout w/o flex or grid is basically one box on top of the next
- em unit is typographically the size (w/h) of the uppercase M
- margin properties can be used to move the element around (does not reflow previous elements, so a margin-top: -50px can put the element on top of the previous block)
- rarely used text flow properties: 
  - word-spacing
  - text-indent (indentation of first line of element / paragraph)
  - text-transform
  - text-shadow
- background-size
  - cover: makes image as small as possible while still covering the whole element (no strteching of either dimension, overflow is invisible); sometimes combined with background-position: center to show mainly center part of image
  - contain: whole image is displayed, possible leaving empty space
  - one pixel value: sets width=pixel + height: auto, 2 sets w/h
- display: table / table-cell is an easy way to give elements the same height (table on parent and table-cell on children); lets us use table-only css properties like vertical-align: middle; better backwards compatability than flex / grid, though flex should be prefered
- picsum.photos is a thing i keep forgetting about
- images are inline elements by default; that's why they have by default baseline padding at the bottom according to the font size; should be changed to block in most cases or wrapping it in a figure tag, which is block level by default
- position: 
  - default: static (placed in normal flow of content)
  - relative: 
    - lets us use top / right / left / top to move element relative to its original position in the flow
    - makes it a reference element for absolute positioned elements within
  - absolute: allows use of top / right etc, pulls element out of flow of document so it leaves no "hole" like relative; positioning relative of document or containing relative element
  - fixed: like absolute but positioning is relative to *viewport* (currently visible part of document)
  - sticky (limited browser support): like absolute until it hits edge of viewport, then like fixed
- Float based layout
  - shouldn't really be used anymore for more than their intended use (image floating or maybe 2 breakable columns for easy mobile friendly layout) unless older browser support (non-flex) is required
  - float: left/right: float adjacent content right / left; makes browser unable to calculate height of containing elements when boxes are floated side by side; defaults to non-floated contents height
  - clear: left / right / both / none: element can't have floated content on specified side (so it breaks as a new block below)
  - "clearfix": solves height calculation problem (google it when needed, whole float designing is kind of deprecated)
- Pseudo elements: 
  - alter display / behaviour of part of content inside element box
  - are regular css boxes themselves
  - ::before, ::after add content
  - ::first-letter, ::first-line self explanatory (use for drop caps for example)
  - ::selection: allows style of user selected text (needs vendor prefix for firefox)
 