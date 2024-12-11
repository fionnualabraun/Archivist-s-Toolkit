#instructions #github #staticsite #commandline 
Began by downloading and opening GitHub for desktop and launched my account through this app. 
Installed command line software in order to run the codes provided in the online tutorial in terminal -- experienced some issues in getting it to install, but if you close out Terminal, then you can accept the T&C and the software will begin to install.
	Something to remember: when you run code, wait for all the text to stop appearing on the screen, and your username to pop up again. This means you can run your next prompt!

The first time I tried to install Homebrew, it returned an error 404, but I solved this by going directly to the website and copying the line of code from there, which allowed me to install (was the code on the tutorial obsolete/old?). Had to run an extra command through to add Homebrew to my path, took a few times to run it as one line instead of two, but got it to work.

Permissions error trying to install rubygems-update, had to do a bunch of Googling before I discovered that my machine didn't have rbenv installed, installed through Homebrew and still didn't work:
- Ran the command 'which ruby' which informed me I was using the Ruby preinstalled on mac, which apparently you don't want to use
- Reinstalled ruby using a separate set of instructions https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/#start-here-if-you-choose-the-long-and-manual-route which allowed me to move away from the bin ruby to the one I actually wanted

Continued on in the tutorial to install node and jekyll.
## Setting Up and Running Jekyll
Switched to my GitHub (not github with no capitals, not sure what's the deal with that) folder, in which I created a folder called DigitalHist. _Tip: cd command allows you to change directory to whatever folder you want to work in.

Fixed site not running by changing port from 4000 to 4001 in config, can now update using command 
```
bundle exec jekyll serve --livereload --port 4001
```

Now I can access my updated site online by going to localhost:4001/DigitalHist/ (had to fix to put a space in the port number and the :

Remember that when you run the site, you first have to cd to DigitalHist, and then submit the command above in order to get it to run.

Followed the instructions to import to GitHub, this was all fine. However, I am stuck now because I can't access my site even after publishing it and making it public on GitHub (the link that the tutorial gives doesn't work) -> ask about this in class #question #answered needed to add https:// before the link, so visit https://fionnualabraun.github.io/DigitalHist/