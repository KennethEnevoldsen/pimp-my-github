
# Pimp your Profile Checklist

Any properly pimped GitHub should naturally have:
- [ ] Personal readme (optional)
- [ ] metadata filled out
- [ ] no stale project
- [ ] relevantly starred project

## Creating a Personal README
A good place to start is using the [profile readme generator](https://github.com/rahuldkjain/github-profile-readme-generator). The way you add the readme to profile is to create a repository with your own name (e.g. KennethEnevoldsen) and then a button will appear in the upper right corner for you to add it to your profile.

## What is a Stale project?
A stale project is a project which content is boring. I.e. it is not something you believe is worth sharing. Typically though these project just needs to pimped up a bit.

## What projects are relevant?
Projects which you would be glad for your new employer to see as their first impression of you. Things you are proud of. Any relevant project should naturally fullfill the [Pimp your Project Checklist](pimp-your-project-checklist)


# Pimp your Project Checklist

Any properly pimped GitHub project should naturally have:
- [ ] Meaningful content
- [ ] A pimped README.md
- [ ] A LICENSE.txt
- [ ] A good folder structure
- [ ] A good name
- [ ] A description
- [ ] No junk files

## What is a good repository name?
There is no strict rules here, but as all good titles it should describe the content and be memorable. This is probably the hardest part. The easiest part is following a convention. Typically GitHub repositories use "`-`" as space and lowercasing the entire title. E.g. [detecting-political-biases-using-sentiment-analysis](https://github.com/KennethEnevoldsen/Detecting-Political-biases-using-sentiment-analysis).

## What is a good folder structure?
While there (again) is no hard rules there is some good guidelines out there. I would suggest using a standard outline and changing that as needed. Some popular examples include:

- [Cookiecutter data science](https://drivendata.github.io/cookiecutter-data-science/)
- [ProjectTemplate for R](https://github.com/KentonWhite/ProjectTemplate)
- [niceRcode](https://nicercode.github.io/blog/2013-04-05-projects/)

Or steal what you find useful. This is to make it easier for you not harder.

## What is a junk file
Junk files are typically temporary files or files which clearly indicate lack of structure. E.g. having the scripts `Analysis1.rmd`, `Analysis2.rmd` and `Analysis2_final.rmd` indicate this. It makes it also makes it hard for you to find what you are looking for when going back. Junk files also include files which does not need to be shared (or worse shouldn't e.g. due to privacy). Examples of these include the `.Rproj` files.

# Pimp your README Checklist

Any properly pimped README should naturally have:
- [ ] Properly formatted headings
- [ ] A visualization, e.g. image or gif
- [ ] relevant shields
- [ ] a project name and intro (and potentially a logo)
- [ ] an explanation of why the project is relevant
- [ ] A "getting started/requirements/dependencies" section
- [ ] Contact information e.g. using Social Icons
- [ ] Use visual hints appropriately
- [ ] <s>A table of content</s>

A good source for inspiration is [this list](https://github.com/matiassingers/awesome-readme) of awesome readmes.

## Properly formatted headings and tables of content
GitHub automatically created a table of content based on your heading. It is thus relevant to use reasonable headings.

Headings generally follow a an overall structure somewhat like this:
```
# Project Name

# Introduction
Describe very briefly but clearly what the project does and why does it exist?

# Getting Started/Requirements/Prerequisites/Dependencies
How to install it, or what packages is used for it (any notable dependencies)

# Acknowledgements/Thank you

# TODOs/Next steps/Features planned

# Contact
```

This roughly follows [Zalando's readme template](https://github.com/zalando/zalando-howto-open-source/blob/master/READMEtemplate.md#readme).

## Including vizualisations
Examples of visualization includes tables, images, and gifs.

### Images
Images in the readme is very useful, but they should typically be used sparsely.

Images and gifs can be included using the following syntax:

Using a markdown syntax
```
![](img/your_image.png)
```

or using HTML:
```
<div align="center"><img src="img/your_image.png"/></div>
```

Generally the HTML is more customizeable.

### Gifs
Gifs is a great way to show interactions with software and they are quite easy to make. Use your favorite video capturing software (on macOS you can use `CMD+shift+5`) and then use an [online converter](https://www.onlineconverter.com) to convert it to a GIF.


### Tables
Tables can be made in markdown using the following syntax. However, unless it is a very simple table I would use a script for creating the table as an image (e.g. using `kableExtra` in R) for creating and image and inserting that instead as it typically allows for more flexibility.  

```
| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |
```
would produce the following table:
| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

## Shield
A [shield](https://shields.io) is meta data denoting symbol. These look quite fancy but are very useful for denoting simple information. E.g. the Python version used:

[![describtor - e.g. python version](https://img.shields.io/badge/Python%20Version->=3.6-blue)](www.desired_reference.com)

which is produced using the following:
```
[![describtor - e.g. python version](https://img.shields.io/badge/Python%20Version->=3.6-blue)](www.desired_reference.com)
```

You will note that this look very similar to inserting an image. That is because it is exactly that:
```
# adding image:
![](LINK_TO_IMAGE)

# adding clickable image with a link
[![](LINK_TO_IMAGE)](YOUR_DESIRED_LINK)
```

The only read trick is the link. Which is basically your desired text as an URL in a two block format, followed by a color: `MY TEXT-TEXT-COLOR`
```
![](https://img.shields.io/badge/MY%20TEXT-TEXT-green)
```
which produces:

![](https://img.shields.io/badge/MY%20TEXT-TEXT-green)


These can be automated quite a bit. E.g. if you publish a package you can have it read the package and software versions from the package publications. You can read more about shields in the shields [website](https://shields.io). 

## *"Getting Started"*-section
The getting started section. typically include how to download the project and install relevant package. For most R project this is not really something which people are in the habit of doing, but for python projects you should always include a `requirements.txt` which indicate the required packages (and potentially their versions number). In R you can do something similar. After you have run the script you can use:

```r
sessionInfo()
```

```
R version 2.15.0 (2012-03-30)
Platform: x86_64-pc-linux-gnu (64-bit)

locale:
[...]

attached base packages:
[1] graphics  grDevices utils     datasets  stats     grid      methods   base     

other attached packages:
[1] ggplot2_0.9.0  reshape2_1.2.1 plyr_1.7.1    

[...]
```

I highly recommend always attaching this to a project as this make it possible for you to see why something which previously worked doesn't work anymore.

This section should also include other potential things you need to install. It is probably relevant to note here
```
single line code can be included using backticks: `2+2`

while multiple lines of code can be included using three backticks e.g. (exlude the #)
#```python
#for i in range(10):
#    pass 
#```

The python here denote the syntax highlighting (the coloration of the text)
```

## Contact information and Icons
Every page should include contact information, even if it is just a reference to the issues section. However you can pimp these up quite easily using icons. This is very similar to using shields so read that section first.

Again we want to create a clickable image:
```
[![](LINK_TO_IMAGE)](LINK_ON_CLICK)

if you want a bit more control of the size:
[<img align="left" alt="Hover over text" width="22px" src="LINK_TO_IMAGE" />][LINK_ON_CLIK]
```

[<img align="left" alt="KennethEnevoldsen | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][https://www.linkedin.com/in/kennethenevoldsen/]



</details>

[twitter]: https://twitter.com/KCEnevoldsen
[linkedin]: https://www.linkedin.com/in/kennethenevoldsen/

<!-- 
# How to readme
- Heading
- check boxes
- code, bold, italic, links, images
- HTML
  - centering
  - images (extra)
  - foldable menus
  - 


# Additional
-  Making rmd viewable on github
-  creating gifs
- how to steal from other peoples github    
-->