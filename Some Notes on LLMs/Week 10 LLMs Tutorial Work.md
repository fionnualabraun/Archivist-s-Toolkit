[[Week 10 LLMs Class Notes, Cool But Not Magic]] for the notes I took during class.
### Environment
There is a huge environmental cost associated with training LMs, but I don't understand why? Is this what it takes to power the machines responsible for the LMs? Get the workers to work? Power the physical storage for the computer? All of the above? There's so much discourse around this at the moment, but no one really seems to go into detail about what's actually making these things so environmentally costly. Are they significantly more costly than other high-powered computing operations? #question -> it's the cost of computing (basically whenever your computer fan whirs you kill a penguin) #answered 
Good point about the fact that countries who suffer for the environmental issues caused by training LMs likely won't benefit substantially from things like ChatGPT.
### Training Data
Data is large and uncurated, this amount of data doesn't guarantee accuracy -- quite the opposite. The internet itself also isn't an evenly distributed cross-section of society (overrepresents young people, people in USA, Europe, Canada, males). Risks perpetrating dominant viewpoints and suppressing viewpoints that use language not considered 'appropriate' by the dominant (could be good, could be bad, depending on the viewpoint.)
LMs trained on large and uncurated datasets encoded views about society that were harmful and marginalizing.

There is no meaning behind the AI's responses, in the way that there is meaning behind a human response. When only one side of the 'conversation' has implicit meaning, then the person conversing with the LM will assign the meaning to what the machine says that mostly closely fits their own worldview (confirmation bias through the roof).

*I ran some highly biased questions through ChatGPT, just to see what kinds of responses I would get. Stuff like "should I vote for Donald Trump" or "are white supremacists terrorists." What I got back equivocated alarmingly -- obviously LMs shouldn't show bias for or against these things, but one would expect that they would demonstrate facts as these facts were demonstrated other places. Interestingly, the prompt "was the 2020 election rigged" came back emphatically as no, so it appears to only equivocate on some issues.*
### LLMs More Broadly
Love this: "Luddites weren’t against technology; they were against the unequal and unfair distribution of those technologies such that their work, their labour, their value was diminished or destroyed. They were against the concentration of power in the hands of the people who deployed the technology. The current deployment of large language models by businesses caught up in the hype cycle is ripe for a neo-Luddite movement. Hell, I’m a neo-Luddite. I do not think these models should be used in the way that they currently are – as tools to reduce human labour and human creativity."

We don't have the ability to get rid of AI, and we largely aren't teaching people how to use it effectively -- instead banning its use etc. What does this teach students about...
- Using tools available to them ethically?
- Navigating a constantly changing world?
- The willingness of the academy to embrace change?
- The importance of integrity and honesty in academia?
### FOMO and LLMs
We're so at the opposite end of this in academia -- still writing about how "There Is No Alternative" to traditional modes of doing things. But the rest of the world is pretty insane in terms of AI being integrated into everything lately (am I the only one who really doesn't want my phone and laptop constantly prompting me to write with AI because the stuff I write is just way too weird for any AI to ever predict it???)

Interestingly, I have found JSTOR's window that predicts future reads you might enjoy to be quite helpful. Maybe it's gotten better. That's actually something I can get behind in research because you still have to do the heavy lifting of reading, but it takes away some of the time you spend messing around trying to perfect your search terms to find a thing you know is true, but need a citation for (obv this isn't always the case and we discover new things doing research ALL.THE.TIME but even then having a little road map of where might be helpful to go next is still nice to have, whether or not you use it).
### To Do...
I ran the first lesson in Google Collab because I wasn't interested in running my computer quite as hard as would've been required for this project.
- Got an error for DeepSpeedPlugins, but it was because DeepSpeed wasn't installed. Went ahead and installed that, ran the second command again. Still an error in that it couldn't find aitextgen. Ran this a couple different ways, restarted the kernel, still no luck, so I tried some of the fixes from this Github forum: https://github.com/minimaxir/aitextgen/issues/215 however none of these gave me what I wanted either, although I think it may be an issue with Collab and the most recent update of Deepspeed, so I tried running it locally instead
- Running it locally worked, but I couldn't figure out where to upload the file so that it would run with Jupyter (Jupyter doesn't appear anywhere in my directory???) so I think this may be a question for tomorrow in class... #question 
- Update, I was able to find Jupyter in my Library, but when I followed the pathway, I couldn't find anywhere to store the text file, so we're back to square one. Having spent several hours trying to troubleshoot this, time to ask!

### Chronicling America API Notebook
This notebook was fairly straightforward for me to use. Struggled a little bit to find the API key for the site, but I returned to last week's tutorial, which allowed me to extract a key which I could input into the section where it stalled out for me the first time, waiting for me to input one. I also tried a few different questions:
- How were fears of HIV/AIDS framed in San Francisco during the early 1990s?
- What was reporting like on moonshiners in the Appalachian Mountains, in any time period?
- How has fear been demonstrated in coverage of American elections, particularly during the 20th century?
Not all these gave me back what I was looking for, but it was really interesting to try. I feel like using APIs in tandem with AI would be a project in and of itself, though -- not so much a research assistant at this stage, more of an entire thesis to chronicle methodology and what worked/what didn't, much like we saw in the readings this week.

### Tetrachs Demo Fix
Fix to ValueError: 

import gpt_2_simple as gpt2
from datetime import datetime
sess = gpt2.start_tf_sess()
gpt2.load_gpt2(sess, run_name='run1')
file_name = "petrie.txt"