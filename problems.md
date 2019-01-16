
## Problem: " 'javac' is not recognized as an internal or external command "

The issue might be that you have another version of the Java runtime environment (JRE) that is being looked up instead of the version of the Java SE development kit (JDK) that you just installed. There are a couple of possible reasons for this.

1. It might be because you did not use `Move Up` to move your new entry to the top of the table in Step 5 of Part 5. Follow all the steps again in Part 5. If you see another entry in the table for Java in your path, (e.g., c:\Program Files\Java\jre-10.0\bin) either delete that other Java entry or just make sure your new entry is higher in the table by using ``Move Up``.

2. It might be that you did move your new entry to the top but you did not enter the path correctly. I noticed that some people decided to install Java in some random place rather than just letting the installer pick the best place. If you did this, delete what you installed and start over again at step 4, allowing the installer install Java where it wants to. Continue with the instructions and make sure that you add an entry to the path environment variable that corresponds exactly to that installation location, which will probably be something like `c:\Program Files\Java\jdk-1.8.201\bin`. Then follow the instructions immediately above in item 1.

## Problem: "Please tell me who you are" when trying to push to GitHub

In theory, Atom comes with full git support, but it appears it might not be working for some Windows users. Here are some instructions that I found on the web.

1. Quit Atom.

2. Install git from here: https://git-scm.com/downloads

3. Go to cmd, as you know how to do.

4. Type the following but replace `youremailaddress@bc.edu` with your actual email address.

```bash
git config --global user.email "youremailaddress@bc.edu"
```

5. If that works, then type the following but replace `Your Name` with your name.

```bash
git config --global user.name “Your Name”
```

6. Relaunch Atom and try pushing your changes again. 

If steps 4, 5, or 6 did not work, just use the [GitHub Desktop app](https://desktop.github.com).

# Mac OSX
"unable to push, error 403"
## Problem: "unable to find remote helper for https"

The issue is that there is a missing dependency for git that arose in a recent OSX update. If you got a lot of chat from your computer about Xcode or developer tools, it was probably your operating system trying to get that missing dependency for you. Here are some possible solutions:

1. Delete you repo that you cloned in class. Then you'll re-clone it using SSH instead of HTTPS. Here's how: when you click on the green `Clone or Download` button in GitHub, in the little window that pops up, you see in the upper right corner `use SSH`. If you click `use SSH`, you'll get a slightly different link. Copy that link, and then clone from that within Atom. Make a change to the java file, and try staging, committing, and pushing your change.

2. An alternative: open a Terminal, and type the following, and then select `Install` and continue to follow the prompts. (Note that this might take a long time!)

```bash
xcode-select --install
```
If neither 1 nor 2 above worked, just use the [GitHub Desktop app](https://desktop.github.com).



