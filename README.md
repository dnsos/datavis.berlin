# Data visualisation Berlin

Here, you find the source code of the website of the Datavis Berlin hosted at [datavis.berlin](https://datavis.berlin). The website is build with build with [Hugo](https://gohugo.io/) and deployed on [Netlify](https://netlify.com/).

The website is an open list about everything related to data visualisation in Berlin. Feel free to make a pull request if you want to add someone, a company, a place, a meetup, …. If you are not familiar with coding you can also contact me through jonas-at-datavis.berlin or on [Twitter](https://twitter.com/zeto). Of course, you can also contact me for any mistakes, suggestions, corrections, …

## Adding an item
All the items are listed in yaml-files in the `/data` folder. Usually, each item in the list follows the same structure:

*Source*
```yaml
- [Jonas Parnow,https://twitter.com/zeto]
```

*Output*
>[Jonas Parnow](https://twitter.com/zeto)

The first item in the array is the text that is going to be displayed. The second item is the link.

### Multiple links per item
If you want to add multiple links per items, you declare the item as array with all the links inside. The first link is displayed normally; all the following are in parentheses.

*Source*
```yaml
-
  - [Universität der Künste,https://www.udk-berlin.de/]
  - [Digitale Klasse,http://digital.udk-berlin.de/]
  - …
```

*Output*
> [Universität der Künste](https://www.udk-berlin.de/) ([Digitale Klasse](http://digital.udk-berlin.de/), …)

### Programmes
Programms follow a slightly different syntax:

*Source*
```yaml
- [FH Potsdam,Urban Complexity Lab,https://uclab.fh-potsdam.de/]
```

*Output*

> FH Potsdam: [Urban Complexity Lab](https://uclab.fh-potsdam.de/)

Here, every item consists of three elements. First the institute, then the label and then the link.


## Adding a job offer
Every job offer is a file in the `/content/jobs/` folder. You can a new job with Hugo with
```bash
hugo new jobs/unique-job-name.md
```
Without Hugo, just create a file with a **unique job name** (for example `sapera-design-director-2020.md`) in the `jobs` folder.

Inside this file, fill out the following fields:
```markdown
---
# Title to be displayed with a short description (max. 110 characters)
title: "Design Director UI/Data Viz (full time) M/F/D"
# Date you added this job
date: 2020-04-08T13:22:57+02:00
# Date when job offer should disappear from the website
expirydate: 2020-06-01
draft: false
# Name of the company (with department if you want) (e.g. "Wikimedia Foundation, Technology")
place: "Company name"
# Date when the job will start; leave out if starting is flexible; afterwards the listing will disappear (date format "2020-02-02" YYYY-MM-DD)
start: 2020-02-02
# Direct link to the job offering (e.g. "https://boards.greenhouse.io/wikimedia/jobs/2083317?gh_src=fd611a951")
link: "https://boards.greenhouse.io/wikimedia/jobs/2083317?gh_src=fd611a951"
---
```

## Adding a translation
That would be super good :)

The files that need to be translated are [content/_index.md](content/_index.md), [i18n/en.toml](i18n/en.toml) and parts of [config.toml](config.toml). All can be opend in a text editor.

In the first TOML file, the part after `other =` is where the translation goes. The part above is the key, where the text is placed. You don’t need to worry about that.
In the Markdown file, the `title` and everything after the three dashes needs to be translated.
In the config TOML file, these parts are relevant:
```
LanguageName = "English"
description = "An open list to the data visualisation scene in Berlin. All people, things and places that are related to visualisation, infographic, data art, data journalism, reasearch, and data tools are welcome!"
keywords = "data visualisation visualization design infographic infromation graphic data-driven journalism ddj interfacedesgin"
```

You don’t need to worry how to add the language. Just contact me and I’ll take the translated files from there.
If you need more guidance, feel free to ask me :)

## Log
- 10.4.2020: [Contentonauten](https://www.contentonauten.de/) added
- 10.4.2020: Spektrum Berlin removed
- 15.5.2020: [Mila Frerichs](http://milafrerichs.de/) added
- 29.5.2020: French translation added
- 29.5.2020: [Sara Akhlaq](https://twitter.com/alltheakhlaq/) added
- 29.5.2020: Christopher Pietsch website added
- 29.5.2020: [Tori Boeck](https://twitter.com/toridykes) added
- 2.6.2020: [Burak Korkmaz](https://twitter.com/BKorkmaz_KD) added
- 3.6.2020: [Arran Ridley](https://twitter.com/arranarranarran) added
- 3.9.2020: Hochschule Hamm-Lippstadt added
- 3.9.2020: Weizenbaum Institut added
- 14.9.2020: [Cédric Scherer,https://cedricscherer.netlify.app/] added
