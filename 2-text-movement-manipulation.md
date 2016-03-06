# Text movement and manipulation

Most people know about copy-paste, but did you know...


### If you copy or cut without selecting anything, it takes that line automatically.

Copy this text from here
Lorem ipsum dolor sit amet, consectetur adipiscing elit.


to here, without selecting anything
Copy this text from here


now try cutting it to here
Copy this text from here

************************

### What that means is that often the fastest way to delete a line of text is simply to cut it...

  def method
    do_stuff(x)
    mistake_line(y) #get rid of this via cut
  end

### ...though if you want to maintain what's on your clipboard, you can still delete with Ctrl-Shift-K.

def method
  do_stuff(x)
  mistake_line(y) #get rid of this via delete
end



##### Remember, the recurring theme is that you DON'T have to have anything selected for these shortcuts to work!

************************

### Paste and indent
If we just copy the baz method into our class below, the indentation looks funny

def baz
end


class Foo
  def bar
  end

end


If we use Command - SHIFT - V, it fixes the indentation automatically!  *****************REMEMEMBER ME!*******************

def baz
end


class Foo
  def bar
  end

  def baz
  end
end

************************

### to duplicate text, make a selection and press control-shift-d.

Lorem ipsum dolor sit amet, DUPLICATE ME, consectetur adipiscing elit.

### to duplicate a whole line, simply do that without making a selection.

Lorem ipsum dolor sit amet, consectetur adipiscing elit.


************************

### to move a line or lines, hold command-control and then press up or down. Again, you don't need a selection to do this.

def baz
end


class Foo
  def bar
  end

end



************************

### if you have long paragraphs wrapped on a single line, and you actually want them to be separate lines, use command-option-q. No selection necessary.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus mattis est varius ullamcorper imperdiet. Donec at vestibulum magna. Integer viverra, massa in scelerisque lobortis, ligula tellus lacinia augue, sit amet faucibus dui est vitae quam. Mauris tincidunt ipsum a condimentum vehicula. Etiam non elit id felis consequat dictum ut vitae erat. Etiam id tortor efficitur, maximus nulla pellentesque, consectetur sem.

Converts the above to the below:

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus mattis est
varius ullamcorper imperdiet. Donec at vestibulum magna. Integer viverra,
massa in scelerisque lobortis, ligula tellus lacinia augue, sit amet faucibus
dui est vitae quam. Mauris tincidunt ipsum a condimentum vehicula. Etiam non
elit id felis consequat dictum ut vitae erat. Etiam id tortor efficitur,
maximus nulla pellentesque, consectetur sem.


************************

### Indentation! Use command-[ and command-]. You do NOT have to select the line for this to work - doing so just wastes time!

Here's my unindented
  And some indented code
    What an amazing
  Thing
Yes



************************

### Comments! Use command-/. No selection necessary. Sublime is (usually) smart enough to figure out what kind of comment is appropriate for the file you're in.

def foo
  stuff(bar)
  more_stuff(baz)
  comment_out_this_line
end

### While you can comment out multiple lines with command-/, if you specifically want a block quote, use command-option-/

It doesn't appear to do anything different in markdown files, but there's a difference in formats where block quotes are supported.

def foo
  stuff(bar)
  more_stuff(baz)
  comment_out_this_line
  and_this_one_to
end


************************

### Transpose: highlight two blocks of text and use control-t to switch them!

switch this text here


with this text down here



************************

### Join: command-j will join your current line to the one below it
In the example below, if you decide that it would be simpler to just assign "something else" in one line to bar, joining lines is probably the fastest way to do it.

def foo
  bar = "something"
  baz = " else"
  return bar + baz
end



