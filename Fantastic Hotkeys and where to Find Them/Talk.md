# Fantastic Hotkeys and Where to Find Them

Sadly(?) this talk is going to be a little Windows-centric.
Most of the ideas and even key combinations do translate but might need a little extra work!
Ctrl on windows ---> Control on Mac
Alt on windows ---> Option on Mac
Windows button ---> Command on Mac
Most hotkeys are at least similar across different applications though technically any app can choose which to implement and what names to give them.

## Step 0: The Basics

- Ctrl + C Copy

- Ctrl + X Cut

- Ctrl + V Paste

- Ctrl + F Search for text

- Ctrl + A Select all text around cursor

- Ctrl + Z Undo

- Ctrl + Y Redo (indecisive much?)

- Ctrl + Alt + Delete Save the day (command + option + esc on Mac)

- Alt + Tab Change window

Being adept at using keyboard shortcuts will stop you reaching for the mouse that much. It may not seem like much but it does improve how quickly you can carry out activities and reduces the chance of getting sidetracked.

## Step 1: You need to go Hunting

Hotkeys won't always announce themselves - you do have to make the decision to seek them out.

If you notice yourself doing the same sequence of actions and it takes long enough for you to notice then that's a sign that there is a better way. Sometimes it is hotkeys you need!

First step - discard your mouse and tape up your trackpad (you can disable it in your computer's settings but I hope an honesty policy will work here!)

You might be thinking - oh no! I don't know how to use my computer now. WRONG

Press the windows key on Windows and type in the name of a web browser of choice.

On Mac you will have to settle with using TWO keys: Command + Space

Most web browsers will automatically put the cursor in the url/searchbar so you can now search for hotkeys to do whatever you need!

## Step 2: The Adventure Begins

You were expecting more than that?

## Real Step 2: Out of the Frying-Pan into the Fire

Do the following while only using your keyboard:

- Open VSCode Windows Key -> VSCode
- Open a new VSCode window Ctrl + Shift + N
- Create a file and put a couple lines of text in it Ctrl + N
- Save the file Ctrl + S
- Navigate to a VSCode terminal Ctrl + '
- Print out the text from your new saved file using your favourite terminal command

Hint: Use google

Different hint: what happens if you hold down the Alt key in VSCode?

Even differenter hint: What happens if you search for `shortcut` after doing Ctrl + Shift + P?

## Step 29786: Inside Information:

## How was that?

Chrome you may have used:

- Ctrl + T Open a new tab and go to it
- Ctrl + F Search for a string in the current page
- Ctrl + E Focus on search/address bar
- Tab (+ Shift) Cycle through page's links

Also useful in Chrome:

- Ctrl + N Open new window (with new tab)
- Ctrl + +/- Zoom in/out
- F12 Open Browser Dev tools
- Ctrl + W Close current tab
- Ctrl (+ Shift) + Tab Change current tab
- Alt + Left/Right Go back/forward
- F5 Refresh
- Ctrl + F5 Hard refresh (ignoring cached info)

---

VSCode you may have used:

- Hold Alt See shortcuts to open menus
- Ctrl + N Open new file
- Ctrl + Shift + N Open new VSCode window
- Ctrl + S Save current file
- Ctrl + F Search inside current file
- Ctrl + Shift + F Search inside all files in open folder

Also useful in VSCode

- Ctrl + P Search for file name
- Ctrl + Shift + P Open command bar
- Ctrl + Shift + S Save all open files (this may not be on be default)
- Ctrl + Tab Similar to Alt + Tab on Windows
- Ctrl + Shift + E Open explorer sidebar
- Ctrl + ' Show/Hide terminal
- Ctrl + / Comment out selected lines
- Ctrl + B Hide sidebar

---

Windows Terminal:

- Ctrl + C Come on, you know this one
- Alt + Shift + D Split current pane
- Ctrl + Shift + W Kill current pane
- Alt + Shift + <Arrow_key> Adjust size of current pane
- Ctrl + Shift + Arrows Make a text selection words at a time
- Home/End buttons Get to the start/end of the current line

---

---

## Bonus: Git Aliasing

Examples for how to set an alias:

- git config --global alias.co checkout
- git config --global alias.review '!git add . && git stash -m "ReviewStash" && git checkout $1 && git pull && git reset $(git merge-base HEAD master) && :'

If you pass a string you probably need to start it with !git

You can pass arguments into this command eg:
git review <branch_1> <thing_2>
will pass branch_1 into $1 and thing_2 into $2 etc

If you are passing arguments into it then you will likely want to have `&& :` at the end - otherwise the arguments get repeated at the end of the command. (feel free to ask me if you would like any help setting up an alias!)

## Excerpt from my .gitconfig file:

[alias]

last = log -1 HEAD

co = checkout

poosh = push --set-upstream origin HEAD

review = !git add . && git stash -m "ReviewStash" && git checkout $1 && git pull && git reset $(git merge-base HEAD master) && :

return = !git stash -m "IgnoreSafetyReturnStash" && git checkout - && git stash pop 'stash@{1}'

current = rev-parse --abbrev-ref HEAD
