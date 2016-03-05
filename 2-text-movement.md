# Text movement

Most people know about copy-paste, but did you know...


### If you copy or cut without selecting anything, it takes that line automatically.

Copy this text from here
Lorem ipsum dolor sit amet, consectetur adipiscing elit.


to here, without selecting anything


now try cutting it to here

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


If we use Command - SHIFT - V, it fixes the indentation automatically!

def baz
end


class Foo
  def bar
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
