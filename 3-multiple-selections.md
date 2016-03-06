# Multiple selections!

### Multiple selections are one of the most awesome features in Sublime!

Highlight a word and press command d to select the next instance of it
You now have multiple cursors! If you start typing, it'll enter in two places.
If you hit command-d again, it'll select the next instance. Three cursors!
Most normal text entry rules still apply... feel free to experiment. Hit escape to get back to one

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.

### To select all instances in a file, use Command-Control-g.

### If you go to far and wish you could take one back, use Command-u. ## Often can use Command-u to undo

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.

####bathroom break
### If you want to skip some instances, select the instance, then hit command-k before you hit command-d for the next instance. Takes some getting used to.

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### You can also manually add a cursor by holding command and clicking or double-clicking elsewhere... this means you can select totally unrelated words.




************************

Now let's combine the power of multiple selection with copy-paste! Maybe you've seen something like this before?

class Person
  attr_reader :first_name, :last_name, :email, :phone, :address
  def initialize(first_name, last_name, email, phone, address)
    @first_name = first_name
    @last_name = last_name
    @email = email
    @phone = phone
    @address = address
  end
end

that's a lot of repetitive typing... can you figure out how to easily generate the rest of the class from here?

class Person
  attr_reader :first_name, :last_name, :email, :phone, :address
  def initialize()
  end
end


Play around more with this kind of thing - it can save a lot of time since programs tend to repeat a lot of strings, variable names, etc.
################# bathroom break



************************

### Using command-d without a selection is the fastest way to select a full word...

If I wanted to delete or select a super-long word like antidisestablishmentarianism, do I really want to scroll all the way to the beginning or end to do it?



************************


### once you have a selection, you can wrap it with many things just by typing that key


'Put single quotes around me'
"Put double quotes around me"
[Put square brackets around me]
{Put curly braces around me}