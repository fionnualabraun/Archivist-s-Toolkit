## Reading
I found this reading really interesting, particularly as it applies to my own research project on networking. I had previously looked in to trying to build a knowledge graph, but I really struggled to find any sort of practical tutorial that actually would have suited my purposes.

The knowledge graphs in this article are so close to what I wanted to build -- or what maybe would have yielded more information to me than what I built in Palladio. I wish there was a tutorial on how to do this! *Reminder: come back to this article and check for appended codes to try yourself -- maybe not feasible for this project, but could be feasible for future projects.*

- LLMs can be used to draw a set of nodes and edges (relationships) from a large corpus of texts
- Big difficulty with this is just writing a prompt so that the LM will give you what you actually want, as opposed to something close to what you actually want (this, like last week's readings, requires a lot of time be spent on teaching yourself how to teach the model, which doesn't necessarily make it practical for a quick turnaround)
- Although...maybe it does! Because this model did end up saving a lot of time compared to creating these networks/knowledge graphs by hand, and yielded similar results
- #question is the amount of time it takes to learn to train LMs, code for all this, fuss around when the programming doesn't work, worth the time it saves you in the actual review of a large corpus of material?
- #question is this a valid and potentially super useful tool for conducting a broad literature review, like the type that's done in social/hard sciences?

Really good example of how these models can be used as a cog -- although I would say that this verges into intern territory in that it's something I can see assigning to a thinking human with a brain as opposed to a machine. Do we encode certain biases in our own lit reviews? What biases does the machine code that is different to the ones that we do? Which is better? Is there even such a thing as better?
### Class Discussion
Memories become archives, archives become datasets, and at each stage you lose context. LLMs learn these patterns of decomposition.

Worked through Melanie Walsh's tutorial on Named Entity Recognition -- whenever you restart a session you have to re run the imports, but not the installs.

Running this type of tutorial gives you the kind of language to search through Github for something that might run, say, a search of a whole bunch of articles for a scoping review (look into this because I don't want to read all the Covidence articles)

I tried some of this tutorial on my own text files (note because there was no html in these, you can skip the code blocks that look at html) and gosh, I knew there was something that could've done all that finding work for me for the term project. I found out too late! Oh well, now I know for next time...Would be super useful for scoping review!

**Fix your file names:
- Proper file name .txt etc
- No spaces

Also tried nuextract with the Egermaier letters, and I was able to build a context that told me about how he was arrested in France. I just went in and changed the template attributes from jesuit stuff to arrest stuff and I got results like "french police," and that the tone of the letter was "regret." 
This is incredible! And it gave me more **nuanced** data because it wasn't just reading from the New York Times. I found Melanie's to make more sense and gave me more readable data. I'm happy I successfully built a template without any errors, and I think NuExtract gives me better and more interesting results.

**It could be really cool to read the emotions in the letters more broadly, and then mapping this to sound and/or colour!**
### Experimenting...

I ran this week's experiment in Google Colab, which is now my choice for running these sorts of things. I first just tried running the code from the main README file, but this didn't work because the 'requirements' weren't defined, and I couldn't find a folder of them to download.
	I am super unfamiliar with this style of programming vs. the tutorials on the programming historian, so this was baseline a bit confusing for me, as I wasn't entirely sure where to start, and there weren't corpuses of material supplied like the tutorials we've done in past weeks...
But I persevered and tried running the demo.ipynb folder from the Github repo instead. On the first part of the code, I got an error that ModuleNotFoundError: No module named 'langchain_mistralai'

Does this mean that MistralAI has deteriorated in this form? Maybe it's not installed -> tried !pip install mistralai, and it did do...something! 
Sucessfully installed, had to do the same thing with python-dotenv

It gave me the same error on core -- but Gemini told me that it was because I don't have core.py as a file in the same chain as I'm working in, not that I need to install it. Does this mean that this is a file I need to download from somewhere? I did some poking around on the original Jupyter notebook and repo, but couldn't seem to find anything downloadable. Something tells me I'm doing this wrong...

**Whoops, so I didn't read the original blog post thoroughly -- I needed to try a different notebook which would allow me to clone the repo! Jeez. I am tired.**

Okay, now it's working! All the previous errors don't seem to be a problem once I cloned the repo. Does this mean I imported some sort of background code or documentation? #question 

Hmmm...still giving me the error that 'code' doesn't exist. I'm going to ask about this tomorrow, because the solve that Gemini gave me still returns the same error...time to ask for help!

