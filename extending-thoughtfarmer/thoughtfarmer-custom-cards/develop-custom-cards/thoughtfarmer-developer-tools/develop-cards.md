# Develop cards

All commands below can be run from the main root directory. If they are, then you must specify the following command line parameters if required.--folder=cardName  
--site=name  
--id=customPortletTemplateId  
  
**NOTE:** It is recommended instead to change your working directory to the folder of the card you are working on. The folder will automatically be designated and the id parameter will automatically be assigned depending on the configuration for the specific card. All you need to do is specify the site or leave empty to use the 'default' site.

### **Command examples**

Running from the root working directory and deploying a specific card to the default site, using the card's configured id:

```text
grunt deploy --folder=cardName
```

Running the same command from the folder ./cardName:

```text
grunt deploy
```

Deploying from the folder ./cardName to a specific site called "dev" \(not default\):

```text
grunt deploy --site=dev
OR
grunt deploy -dev
```

### Build your project

```text
grunt build
```

**Required parameters:** folder  
Will use the file /cardName/cardName.jsx and /cardName/cardName.scss as entry points. It will then build a cardName.js, cardName.html and cardName.css in the /cardName/dist folder. Files in this folder are the ones deployed to a ThoughtFarmer instance.  
  
The built files will use [rollup](https://rollupjs.org/guide/en) and [Sass](https://sass-lang.com/) to import all external dependencies into these singular files. 

### Lint your JS

```text
grunt check-js 
```

**Required parameters:** folder  
Will ESLint the file ./cardName/cardName.js using the options as set in the .eslintrc

```text
grunt check-jsx 
```

**Required parameters:** folder  
Will ESLint the file ./cardName/cardName.jsx using the options as set in the .eslintrc

### Push changes

```text
grunt push 
```

**Required parameters:** folder, site, id  
Will push the currently built files to the site and id specified. No upgrade is called so the live card at the endpoint will remain unchanged. Use this to get your updates to the server without making live changes.

### Upgrade a remote card

```text
grunt upgrade
```

**Required parameters:** folder, site, id  
Will upgrade the portlet with the id at the site specified \(default if not\). For use when there is already a newer version on the server that is not yet set as the latest version. 

### Build and deploy all changes

```text
grunt deploy 
```

**Required parameters:** folder, site, id  
This command will run the build, push, and upgrade tasks.  


