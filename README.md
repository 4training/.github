## Motivation
4training.net is a website with training resources on following the example of Jesus in more than 40 languages:
- Simple worksheets which are high quality and easy to multiply
- Overcoming language barriers in outreach and discipleship
- Everything is copyright-free (CC0) so that multiplication can happen

Dozens of people have already contributed to that vision in different roles: translators, developers, content editors, feedbackers, ... and people around the world are using the resources to learn and apply them in their own lives and train others in their heart language.
*We're looking for more people who are willing to share their skills and join this vision - maybe you?*

## Development
The [4training GitHub organization](https://github.com/4training) is the home of the IT side of the project. There are different parts:

### Website
The [4training.net website](https://www.4training.net) runs with [mediawiki](https://www.mediawiki.org) (the software that also powers [wikipedia](https://www.wikipedia.org/), written in PHP/HTML/CSS/JavaScript), together with the [Translate extension](https://www.mediawiki.org/wiki/Extension:Translate) - a great technical basis for this big vision. Everyone can use the website to view and download the resources. Translators get a login to translate content into their languages.

#### Repositories:
- *Our main mediawiki repository is currently not public*
- The [ForTraining skin](https://github.com/4training/mediawiki-skins-ForTraining) is the [MediaWiki skin](https://www.mediawiki.org/wiki/Manual:How_to_make_a_MediaWiki_skin) for our frontend. It's using up-to-date technology ([mustache](https://mustache.github.io/)) but it's still the old design from 2015 and we wish for a new, mobile-friendly design.
- The [ForTrainingTools extension](https://github.com/4training/mediawiki-extensions-ForTrainingTools) adds the custom functionality provided by the [Python tools](#python-tools)
- We have some repos with mediawiki extension which we customized slightly: [Translate](https://github.com/4training/mediawiki-extensions-Translate), [UniversalLanguageSelector](https://github.com/4training/mediawiki-extensions-UniversalLanguageSelector), [cldr](https://github.com/4training/mediawiki-extensions-cldr), [CustomSidebar](https://github.com/4training/mediawiki-extension-CustomSidebar)

### App
The [app](https://play.google.com/store/apps/details?id=net.app4training) provides easy and offline access to all the resources on smartphones. It is implemented in [Dart](https://dart.dev/)/[Flutter](https://flutter.dev/) so that development is fast and we only need one codebase and still target two platforms. The app is currently published in the Android Play Store and we plan to have it available for iOS available by the end of 2024 (this is not a technical issue - for that we need to set up an organization as legal entity which takes time...)

The main aim of the app is to serve people who want to disciple others. It is designed to work offline and to be safe to use also for people who are persecuted because they follow Jesus. To ensure that, the app doesn't use any tracking, doesn't need a login and doesn't collect any personal data. It only needs internet access for downloading / updating resources for a language, afterwards they're available offline. The resources are stored here in different repositories (example: [English resources as HTML](https://github.com/4training/html-en), [English PDFs](https://github.com/4training/pdf-en)) so the app only connects to github.com. Additionally this approach improves redundancy and avoids scaling issues as the app is not directly dependent on the 4training.net website.

**Repository: https://github.com/4training/app4training**

### Python-Tools
MediaWiki has a good [API](https://www.mediawiki.org/wiki/API:Main_page) which can be used for automation with ["Bots"](https://www.mediawiki.org/wiki/Manual:Bots). We use the [pywikibot](https://www.mediawiki.org/wiki/Manual:Pywikibot) framework to develop [helpful tools in Python](https://github.com/4training/pywikitools). They have a lot of functionality, improve the quality and also are the "glue" between different components:

- Consistency checks and automatically correct minor translation errors (syntax issues)
- Generate translated PDF files
- Take the worksheet content, transform it and push it into the git repositories that the app needs
- Embed machine translation to help translators and speed up their work
- Generate overviews over translation progress in individual languages
- ...

**Repository: https://github.com/4training/pywikitools**

### Contributing
See also https://www.holydevelopers.net/

Help is appreciated in many different areas: frontend design, dart/flutter, PHP, Python development (also some tasks for beginners). Also we're looking for people who could help with some editing and maintenance tasks (no special development skills necessary!)

For the python tools we have [issues](https://github.com/4training/pywikitools/issues) directly in the repository and use a [public project plan](https://github.com/orgs/4training/projects/4). For the app and other components we use a redmine for project management. That's currently not public but if you're interested in helping out we're happy to give you access!

