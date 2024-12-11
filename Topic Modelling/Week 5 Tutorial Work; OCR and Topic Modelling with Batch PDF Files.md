### [[Week 5 What is Topic Modelling]]
Look here for class notes ^^

Tried to use OCRmyPDF to get information from PDFs recommended on the tutorial, got several errors that appeared to rotate (I would run the same command but get different errors each time):
- Asking me for a 'quote'
- Telling me the files I named didn't exist in my finder, even though they definitely did
- Asking me for an 'output' (when I tried to fix this by indicating output.pdf, then it came back and told me the file it previously read no longer existed)
Only gives 'file not found' error when I try to specify output -- if I don't specify output then it runs.
#question I tried running OCR on all my open files, as well as running several alternate commands including ocrmypdf 'pdfpathway' but all returned the same error. I'll need to get help with this tomorrow.

I did try skipping this step and assuming it happened somewhere in the background, and moving on to turn the pdftotext and -grep searches, but I came up empty handed in my 'labourstatistics|wagestatistics' search.

##### Topic Modelling
I had much more success with this tool! Everything ran smoothly, including setting up the workspace and running the tool using the zip file provided.
Once I ran the tool, however, the topic words it outputted were pretty much nonsense, besides the word 'plaque.' I am wondering if this had something to do with the text formatting coming in. #question #answered 

I was able to do all the things in PivotTable, the only problem was that my topics were gibberish, so it didn't really actually make any sense. This is also a troubleshooting thing for tomorrow, I think. This tool could be incredibly useful to me.

### Update!
Turns out I just needed to unzip the file, and then it got the actual, proper data. Ran again, it works and it's really interesting. Something I could use if I could extract text from images?

When you use the Topic Modelling Tool, you are using something that is no longer in development, so it's largely replicable (even if the results different people get are also slightly different). But for a methods approach, it is much more concrete to describe and allow other scholars to replicate/verify your results.

If you use topic modelling, you can put up all of the .csv files on github and invite readers to explore more about it. 

If you choose not to include certain words in your final topic, that's okay, just look into it and be transparent as to why you chose to disinclude these things. Then, if someone disagrees with you, you at least have something to disagree about, instead of someone just being a nob. 
### Trying voyant-tools.com
I tried running some of my del Boca - Welti documentation through voyant-tools and what it did with topic modelling was absolutely amazing. This is definitely something to use in the future when you're looking over stuff from Arcadie. Some things to note:
- It will be best to have all these files/OCR texts in one place so that they're easier to upload
- Navigate to 'topics' to do topic modelling (keep running until you find something that fits -> remember, this isn't about truth, it's about interpreting in a certain way or finding a new way to see things)
- Navigate to DreamScape in order to get a working map of where all these texts were discussing/coming from
If you want to get rid of stopwords (I'm, dear, etc), go to the toggle button, and then you can create a custom stopword list that you then tick off when you run the topic model.