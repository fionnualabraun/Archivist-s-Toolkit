Used Microsoft Azure Transcribing Services (accessible over the web) so computer can send images to Azure, and then Azure sends back transcribed data. Good in both English and French (limitation here).
- Slightly painful sign-up process to get the free student trial but we got there in the end!
It was pretty easy once I signed up to create and deploy the computer vision thingy, but I have questions about how Azure is using this data since it asked me to sign off on it being used for AI? Do I get a choice in this? I'd rather not have my data being used to train LLMs, even though I know it probably already has...

After this was done, I opened a Python notebook in Google Collab (I like Google collab! How useful. I can't believe I spent the first part of this course doing things only locally on my computer...)
Shockingly, the !pipinstall command worked for me for the first time...woohoo!
Remember to run the third set of code **once per session** if you are using this again -- before you do anything else!
I uploaded an incredibly convoluted 15th-century manuscript to the Collab notebook and ran the fourth example set of code for uploading a folder from my computer and then having it output the text as a plain text file. It did give me an error: 
read_handwriting_in_stored_image is not recognized
And then spat out a blank text file. Sigh. Time to troubleshoot...
- First I tried calling the Azure software in to see if that might work, but then it gave me an internal server error, as well as the original error above
- I thought maybe the text in this file was just too complicated, so I tried it with the sample data provided in the tutorial. This gave me the same two errors again, even though I did it running the original code from the tutorial and not the code that called Azure, which was interesting since that didn't happen the first time. Once again spat out a blank text file.
*Now, I know that my image format is correct because it was the one from the tutorial and I also checked it against what the tutorial said would work, so it wasn't that. I double checked my subscription configuration, and it wasn't that either, so I'm at a bit of a dead end here re. the server error -- internal Microsoft issue? Need some help here* #question #answered 

I decided to try one of the other ways of using the code instead, so I tried the first suggestion. And once again received a server error, which was leading me to think that this was maybe a Microsoft issue. I decided to try running the code locally to see if that would give me better results!

...Which didn't work full stop. When I ran the code, it gave me an indent with >if. When I tried inputting the key, nothing happened, so we're at a dead end here as well.

I looked more into the server error, looks like maybe I need to change the endpoint only to the .com point. https://forum.uipath.com/t/exception-thrown-in-microsoft-azure-computer-vision-ocr/158338/2 Let's try that!
- I made an entirely new Collab notebook so I could do it again without any prior issues related to already having dowloaded the software in the other notebook
- Aaaaand received the same error -> couldn't find any other troubleshooting forums for this particular error online, and the Collab AI was mostly giving me stuff I'd already tried (validating my subscription, etc)
- In the end, I ended up trying all the suggested methods on the tutorial and received the server error every time, so this will need to be resolved tomorrow #question think this might be an issue with the student account, try again next week #answered #followup
To see my many failed attempts, go to: https://drive.google.com/drive/search?q=owner:me%20(type:application/vnd.google.colaboratory%20||%20type:application/vnd.google.colab)
### Practical Stuff:
Key: d387bd2a9c4c4a2e99818a80d40f8e40
URL: https://fbdhtranscription.cognitiveservices.azure.com/

Another issue: when trying to install the Tropy plugin, it greyed out everything I could select, so I wasn't able to install it #question 
### Class Things
- Something incredibly useful: https://huggingface.co/spaces/GanymedeNil/Qwen2-VL-7B for transcribing handwritten text
- PaddleOCR does not work on handwritten text, so don't bother with it unless it's printed
- OCR only gets about one third of the results from the archive, so you shouldn't be citing a digital search the same way as you would be citing a physical search because of these discrepancies
- Historical Text Analyzer on github to make a network out of a text