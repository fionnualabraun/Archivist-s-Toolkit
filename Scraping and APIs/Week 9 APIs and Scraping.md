### What are APIs? Working with Europeana and XAMPP
To be honest, I'm still a bit confused about this. Basically, it sounds like they are a way for websites to communicate with one another, creating a sort of repository that other websites can access so we don't have to build everything from scratch. But, I'm not 100% sure, so this is a class #question 
Assuming my understanding of APIs isn't completely off base, it completely makes sense why researchers would want to use them as a way to give others/gain access to data. This really ties in with what we talked about in our open source research week last week, coming at research through an ethical lens and offering our data to others.

When using the Europeana API, it seems to me that what you can do is access broader datasets that aren't available on the website, by running your API key and then a search term. For example, if you use the search term 'London' you can then look under 'items' (usually where peoples' research interests fall would be underneath the items part of the API search, according to the article). It will also provide you with a lot of information that has bibliographical relevance, like where the item came from, etc. This can be used to describe even physical heritage items, like the Mona Lisa. #question are APIs more useful for categorizing large datasets than actually working with the individual data pieces in that set? It sort of seems this way...
The XAMPP local host reminded me a lot of Jekyll in terms of how it was initially set up and also how it was stored on my laptop. I found the way that this tutorial broke down the coding language and what it was actually doing (as opposed to just giving sections to copy and paste) to be incredibly helpful: https://programminghistorian.org/en/lessons/introduction-to-populating-a-website-with-api-data
It seems to me that with XAMPP you can create a site where you store APIs -- is this correct? #question 
You can turn it into something readable in PHP by using the command json_decode (assuming this is possible with other API readers as well).
You can then go on to build a table of this data (as opposed to a mess of providences, descriptions, etc) by using the following code:
```
print '<hr>';
// Table view of Europeana data
print '<table border=1><tr><th>Title</th><th>Data Provider</th><th>External Link</th><th>Thumbnail</th></tr>';


print '</table>';
```
```
foreach($data_europeana->items as $item) {
    print '<td><a href="'.$item->guid.'">' .$item->title[0].'</a></td>';
    print '<td>'.$item->dataProvider[0].'</td>';
    print '<td><a href="'.$item->edmIsShownAt[0].'">View at the provider website</a></td>';
    print '<td><a href="'.$item->guid.'"><img src="'.$item->edmPreview[0].'"></a></td></tr>';
}
```
Something else that is helpful, particularly if I were to do more work in digital history, was the 'error handling' part of this tutorial. It's helpful to have this as it gives some possible solutions to issues a person might encounter as they're attempting the tutorial.
**Basically, this tutorial allows you to go beyond what the website might offer as a default way to read large amount of data and instead set it up in a way that works for you. I can absolutely see how this would be useful for me.**
### Trying the Colab Notebook
Cool to run this notebook because it showed me everything that I learned about theoretically in the last tutorial in practice. I was able to access the data.json file by going into the files part of the Colab notebook (I am learning new skills!) and although the data wasn't pretty to read, it was there. Is there a way to turn this into a nicer table, like I saw in the last tutorial?
### Fetching and Parsing Data from the Web with OpenRefine
I wasn't able to start OpenRefine because my computer said the developer needed to update the version of it. I'm sending an email, will check back in on this!
### Automated Downloading with Wget
Can be used for mirroring entire websites, or downloading specific files in the website's hierarchy. I was able to install wget through Homebrew with no issues.
You can use the command wget + a URL to download things from the /papers/ part of a website. I did this with activehistory (cool to see on a site I've published on) and it worked! I was able to mirror the website -- success!!

Something else cool about this tutorial was that I was able to learn some 'internet etiquette' about not taking up too much download room on a server, etc, as well as some commands that would help me limit the download room I was taking up. This was interesting and useful since I didn't know there was etiquette about this sort of thing -- but it totally makes sense!

Class notes: [[Week 9 APIs Class Notes]]


