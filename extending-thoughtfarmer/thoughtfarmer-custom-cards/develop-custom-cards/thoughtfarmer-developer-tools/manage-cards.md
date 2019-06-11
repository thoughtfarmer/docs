# Manage cards

### Create a new card

 To configure and create a new card run the following from the root working directory.

```text
grunt newcard
```

The command will ask for:

* **name**: name of the card
* **Use JSX**?: If this is a React card then say yes.
* **Use project scaffolding?**: This will create a structure to allow you to use [import syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) in jsx and js files to split out your card into many files. It will also support [import for Sass](https://vanseodesign.com/css/sass-the-import-directive/). It is highly recommended you use this approach except for trivial small cards. Saying no here will create no sub-directory and all files will be deployed as is with no support for import syntax.
* **ID for site:** This is the custom template ID of this card for the specified site. This question will be asked for every site configured. If you do not wish to add an ID for a specific site just hit enter. To configure IDs of a card for specific sites later you can run **grunt configure.**

Once completed the command will create a folder and files matching the name. This will include:

* _./name/name.html \(if you said yes to html\)_
* _./name/name.js \(if you said no to JSX\)_
* _./name/name.jsx_ \(if you said yes to JSX\)
* ._/name/name.scss -_ this file is always created. This is the entry point for all Sass. 
* _./name/GruntFile.js_ - this file should not be modified and is only to allow for running grunt commands from the child folder.
* _./name/config.json_ - this file contains id to site mappings for this card.
* _./name/components_ - this folder is created if you said yes to project scaffolding. Put all your project dependencies here. You can also add whatever folder structure you like. Just use the import directives accordingly.
* _./name/dist_ - \(if you said yes to project scaffolding\). The existence of this folder tells the tools to expect import syntax and will trigger the rollup tasks. Without it the legacy build mode will run and only the root files will be deployed, no rollup.

### Configure an existing card to connect to a site

You can use this command to connect your code to a new site, or to reconfigure the connection to an existing site.

```text
// from the root working directory
grunt configure --folder=cardName

// from the folder itself
grunt configure
```

The command will ask for:

* **ID for site:** This is the custom template ID for the specified site. It will ask this question for every configured site. You can keep an existing value, or skip an unused value just by hitting enter. Otherwise, enter the ID to associate it for this card for the site. 

### Initialize a project

If you have existing code in a folder \(e.g. ./name/name.jsx, ./name/name.scss\) you can run this command to initialize the files required to begin development. This will add:

* _./name/GruntFile.js_ - this file should not be modified and is only to allow for running grunt commands from the child folder.
* _./name/config.json_ - this file contains id to site mappings for this card.
* _./name/components_ - Put all your project dependencies here. You can also add whatever folder structure you like. Just use the import directives accordingly.
* _./name/dist_ - The existence of this folder tells the tools to expect import syntax and will trigger the rollup tasks. Without it the legacy build mode will run and only the root files will be deployed, no rollup.

```text
// will only work from the root working directory
grunt init --folder=cardName
```

