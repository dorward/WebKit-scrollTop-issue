While working on a project, I found an odd bug surrounding the setting of
scrollTop in WebKit.

Given a box with a height that is a multiple of 21px, a line-height of 21px, and
a margin and padding of 0 everywhere except the bottom of paragraphs (which was
also 21px) and then adjusting the scrollTop of an element by multiples of 21px,
the lines that were visible did not perfectly fit in the container (in WebKit,
Opera, Firefox and NetFront were fine).

I have produced a reduced test case to demonstrate the problem. Unfortunately
it isn't so pronounced here with only a single pixel of overlap (rather then the
~3 I can see in the Project I Can't Reveal Details OF), but I'm hoping the cause
is the same and that someone knows of a solution (or can say that it is a
WebKit bug and that it can be fixed in the rendering engine itself).