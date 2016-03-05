# Snippets!

A snippet is a small chunk of code inserts text for you when you run the code. You can tie that snippet to triggers, so a common pattern is to write some code (like the word lorem), hit tab, and get some text back.


Snippets are really cool! But we don't have time to talk about them, and the process is actually not too hard, so try these as resources to get started.

http://www.hongkiat.com/blog/sublime-code-snippets/

http://sublimetext.info/docs/en/extensibility/snippets.html



# Command Palette

A number of other shortcuts are accessible using command-shift-p. This is called the command palette, and is a great way to:

1. Word wrap
2. Convert cases(upper, lower, title, and if you install the Case Conversion package, many other useful programmer-y packages)
3. Reindent lines
4. and more




# Package control

Package control is the easiest way to install new plugins into your Sublime. First, you have to install it, which is not too bad - go here and follow the directions: https://packagecontrol.io/installation. Make sure you use the code that matches your version! Sublime text 2 is NOT the default.

If that was easy, this next part is a cinch. Let's use an example with one of my favorite plugins: Text Pastry.

Using the command palette (command-shift-p), type 'package control'. You can see a variety of useful options for interacting with your packages. But what we need now is "Package Control: Install Package". It will bring up a long list of packages that are supported with package control. Type 'Text Pastry' and hit enter.

Now we have Text Pastry. No configuration (in most cases, though a plugins github or package control page will usually tell you anything you need to do and give examples of usage). It's that simple.

Text Pastry lets you generate certain kinds of text more easily. I usually use it for numeric sequences. This is a dumb example, but if we need to populate array indexes below, it would be as simple as getting multiple cursors in the array brackets (and hopefully that's easy for you now!), opening up the text pastry command prompt with command-alt-n (or command-function-option-n), typing "i0", and hitting enter. That will start a numeric sequence at 0 and keep going for every cursor you have available.

array[] = "Red"
array[] = "Orange"
array[] = "Yellow"
array[] = "Green"
array[] = "Blue"
array[] = "Indigo"
array[] = "Violet"



# Navigating key bindings

If you can't remember all these shortcuts (reasonable), that's okay. If you go to Sublime Text 2 > Preferences > Key Bindings - Default, you will see a file that lists and determines your keyboard shortcuts. Reading or editing this file is a great way to remember shortcuts, add new ones, and change existing ones.

Let's take a look. The entire thing is basically an array of hashes (it's an array of Python dictionaries), and each one corresponds to a shortcut.

For example:
{ "keys": ["super+shift+n"], "command": "new_window" },

Super corresponds to the command key on Macs. So command-shift-n will open a new window. Try it now.

Cool, right? We won't go into the details, but you can play around with some of the more advanced features, like args/operator or context (which limits *when* a particular shortcut is valid). And obviously there has to be an existing command that corresponds to what you want to do (though I'm sure you can write your own via plugins). But let's add a simple one that uses existing functionality just to show how easy it is.

Remember when I said that allegedly (according to the internet), the shortcut for Goto word was 'Control-;'? It didn't work on my computer though. So let's add it. It will be very similar to the shortcut for Goto Line, which we said was 'Control-g'. So we can actionally search the file for "ctrl+g" to get started. We find this:

{ "keys": ["ctrl+g"], "command": "show_overlay", "args": {"overlay": "goto", "text": ":"} },

So if we hit control-g, it will bring up an overlay ready to do a goto search, with the starting text ":". Adding our own shortcut is a simple tweak.

{ "keys": ["ctrl+;"], "command": "show_overlay", "args": {"overlay": "goto", "text": "#"} },

Just take that second chunk of code and add it to the Python dictionary, and that's it. You made a new shortcut. Try it now.

There's a lot of potential here, but that's the basics! Go forth and shortcut. If you want an additional challenge, try adding a shortcut for expanding selection to paragraph - I haven't done this but I believe the command already exists in sublime, so it shouldn't be hard to put a key binding on it.


# Additional notes

1. Plugins typically set their key bindings under Sublime Text 2 > Preferences > Package settings > Name_of_package > Key Bindings - Default.

2. You can have key bindings that override each other! So watch out. If you end up in that situation, the two main options are to a) just find one key binding and reassign it, or b) add some context to both key bindings so that they only fire in the situations you're likely to use them. There is actually a plugin that will help you figure out where you have key conflicts called - wait for it - FindKeyConflicts.