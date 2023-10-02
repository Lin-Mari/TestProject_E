###### mkdocks intro
### mkDocs and how to use it
This product wad build using mkdocs. If youre unfamilliar with mkdocs dont't worry. 

MkDocs is used to provide some functonality to this project. It allows users to be able to view this book online or alternativly create a PDF version of it for more comfortable reading while offline. Additionally it allows users to "host" a "local instance" of the documentation platform from their onw computer. This i a facny way of saying youre crating a fake web page in your broweser. 

What this allows developers to do is make sure everyting is displayed and functioning as it is intended to to before making the platform live for the world to see. We dont expect you to be doing any developing but it does offer a neat nieche for wieving the platform offline, as if it was online. 

For anyone interested please follow this sections instructions.

# Mkdocs

Mkdoca allows users to create stunning Github static pages for documentation. We used Mkodcs to implement tihs platform. The following is a quick guide to setting up mkdocs and getting started creating you own unique platform. 

> **Note:** *The following are prerequisites for completing the tutorial. `Python` `pip` `VScode` and a `CLI`. Make sure you have the required software by following this [guide]()*

### Getting started with mkdocks

Altough it might seem complex, creating your own mkdocs project is as simple as following these simple steps. Make sure to chect out the [prerequsites]() to ensure you have everything you require to be able to complete this tutorial. you'll nedd an CLI (command line interface) to follow along. I recommend using linux's terminal as it has been the easiest way for me and it will be the tool of choice for this project. Alternativly for windows user you can enable [WSL]() and have access to the same CLI as found in linux. 

Since we want our pages to be availible online we need to publish it. We can do this without paying a hosting provider a lot of money by simply uploading our site to GitHub pages. GitHub allows pages to be hosted through a GitHub repository for free. This functionality was initially developed to help develpment teams create large and complex documentation sets for products they were working on. Although our project wont be as complex as theirs we can still make use of the same facility to publish our documentation.

#### Step 1: We need to create a GitHub repository which will contain all our files.

> **Note:** *A GitHub profile is required to continue with this ttorial. If you do not have a GitHub profile, you can reister for one [here](https://www.github.com/register) for free*

1. Login to your GitHub account.
[login_github]()

2. Select create new repository.
[new_repo]()

3. Complete the required fields.
GitHub requires some information to be able to effectivly create a repository. You can copy what I do or create your own. the choice is yours. 

- **Repository Name:** This is what your project will be called. i would advice sticking to a descriptive name as it would make it easier for people to find your project. I'll call my project `MkDocs-Tutorial` for simplicity's sake.

> **Note:** *GitHub auomatically checks if your repositiry name is availible, you cannot have more than one repository with the same name, just like you cannot have more than one file which has the same name on your computer in the same namespace.*

[naming_repo]()

- **Readme File:** Its best practice to include a readme file in your project. This file should be populated later to provide a brief discription of what your project is all about. The readme file will be displayed when people view your GitHub repository so providing a little informations goes a long way.

- **Lcense:** As your project will be publicly availible, unless you select a private repository, it is a good idea to include a licensce. Spend some time to read through the licneses availible on GitHub and select the one which fits best. I'd like to point out here that a licence in not nessacerry but simply good practice. Skip this step if you would like. Ill select `{insert licence choise here}`.

4. Select create repository

[create_repository_done]()


#### Step 2: Install mkdocs.

Now that we have a GitHub repository we can get to working on the documentation. First wel need to clone our project repository to our computer.

1. From the GitHub repository click on `code`

[clone_button]()

and select the two squares to copy the address.

[clone_squares]()

2. Open your CLI (command line interface), in my case it the terminal. Linux: press `ctrl` + `T`

[cli_new]()

3. Navigate to the desired folder in which you want to store the project by using the `CD` command. I want to store my project in my documents folder, but you can put it wherever you would like. 

```cd Documents/```

> **Note:** *Make sure your inside the correct folder to avoid confusion later. The path is displayed in the terminal as `~/Documents` or `C:/users/{username}/Documents`*

now clone the GitHub repository by using the `git clone` command. You can paste the previously copied path by pressing `ctrl` + `shift` or `ctrl` + `shift` + `V` depending on your OS. If implemented correctly your comand should look like this:

```git clone https://github.com/EliVolsch/Learn-Centre.git```

4. After your repository has been cloned navigate to the newly created directory. 

```cd Learn-Centre```

5. Once inside the directory we can create and activate a vitual environment, by running the following code:

```python -m venv venv```
```scource venv/bin/activate```

notice your terminal has now changed and displays the following `(venv) (base)`.

[terminal_activate_venv]()

6. Lets open the project in VS Code by running the following commad:

```code .```

> **Note:** *Code is the command to lauch visual studio code from the terminal. The full stop `.` indicates the directory. A full stop is the current or active directory*

[vs_code_new_project]()

Select `trust the authors` from wihin vs code.

7. For simplicity's sake well continue working within the vs code terminal. Open the terminal by selecting `Terminal >> New Terminal` from the top pane. Notice the terminal inside vs code has automatically activated the virtual environment since we can see `(venv) (base)`.

> **Note:** *mkdocs support many different themes. For illustrative purposes we'll use the mkdocs materials theme. You can read more about how themes work and using them in your project [here](./mkdocs_themes.md)*

8. Lets install mkdocs by running the following code:

```pip install mkdocs-material```

9. Once mkdocs has completed its run we can create a new project

```mkdocs new .```

this creates a new folder inside of the directory named `{folder}` and file named `{file}`

10. Lets run this to see what it looks like before continueing.

```mkdocs serve```

inside the terminal a message should appear stating `INFO - [14:44:33] Browser connected: http://127.0.0.1:8000/`. This means that you are now hosting the document site on your local machine and can view it like it would be displayed on the web. Hold `ctrl` and click on the link `http;//127.0.0.1:8000` to open your page in the browser.

#### Step 3: Sprucing up the platform

When the browser opens you'll see the deafult mkdocs project page. In many cases this will do but we would like something that looks professional and appealing. Play around on the deafult page before continueing with step 3.

[Deafult_page]()

Mkdocs supports other themes, which dictates how the page looks and react. You can view all the availible themes on the mkdocs [themes](./mkdocs_themes.md) page. Some themes are created for different applications or purposes. You may want to write a blog or have the documentation read like a book. You should find a theme to suit your needs. Alternativley you can also create your own theme and submit it to mkdocs to be listed here.

[mkdocs_themes_page]()

All of the themes are "modular", which means it has a certain level of customisation you can apply to it. For our application well look at the `materials` theme, and customise it a bit to better suite our needs. You can view the [mkdocs-materials]() documentation to get a better sence on how to use it.

For our project we will use the `materials`theme. Currently our project still uses the deafult mkdocs theme, so let change that.

1. In `vscode` locate and open `mkdocs.yml`. This file is the configuration file for our documentation site and contains all the nesecerry information to change the the look and navigation of the documents page. Your file might be empty at this stage meaning all the configurations are set to deafult. Mkdocs wil automatically load defult values if no alternative value is specified in this file, so no need for long and confusing files.

[mkdocs.yml]()

2. Lets add the following to the document to apply the `materials` theme. 

```
theme:
    name: material
```
for a complete list of all possible configuration codes and their corresponding effects you can view the [mkdocs materials setup](https://squidfunk.github.io/mkdocs-material/setup/) page.

3. Now save your work and view the changes. 

> **Note:** *This might cause the local instance to "crash". Dont worry as this will not harm your computer in any way. If this happens you can run `mkdocs serve` again to lauch the local instance.*

[mkdocs_material_first_view]()

4. Now our new theme has been applied. We can make some additional changes to the mkdocs.yml to add some more functionality and change some looks. Lets change the file contents to this:

```
site_name: mkdocsTutorial
site_url: "https://github.com/EliVolsch/{link here}"
theme:
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - toc.integrate
    - navigation.top
    - search.suggest
    - search.highlight
    - content.tabs.link
    - content.code.annotation
    - content.code.copy
  language: en
  palette:
    - scheme: default
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to dark mode
      primary: teal
      accent: purple
    - scheme: slate
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode
      primary: teal
      accent: lime
```

Explanation:
```
features:
    - navigation.tabs
    - navigation.sections
    - toc.integrate
    - navigation.top
    - search.suggest
    - search.highlight
    - content.tabs.link
    - content.code.annotation
    - content.code.copy
```
Here we are making some djustements to the styling and making improving some of the features. A more detailed list can be found [here]()

```
Language: en
```
making sure the language is set to english

```
  palette:
    - scheme: default
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to dark mode
      primary: teal
      accent: purple
    - scheme: slate
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode
      primary: teal
      accent: lime
```

changing the deafult colors of the platform, and icluding a toggle button to switch between ligh and dark modes.

5. Now save your document and have a look at what has changed.

![mkdocs_changes]()

#### Add aditional pages
We currently only have one page in our project. Although we can put all the information about our project into this page, we also have the ablilty to creae more pages, and sections to store those pages in. Lets add a new page to our project.

1. From `vscode` using the file explorer we can navigate to the docs folder and create a new file using the `+` icon. Call it whatever you like but make sure to add the extension `.md` at the end and press enter. 

![markdow_add_icon]() ![markdown_file_add_name]()

Aditionally you can also create new files from the terminal if `cd` to the correct folder. Simply run the following commands:

```
cd docs/
touch page2.md
```
![terminal_command_cd]() ![terminal_command_touch]()

2. once a new file has been created you can open it in `vscode`. This gives us a blank markdown page, which we can add content to. If you are not to fammiliar with markdown syntax you can read more [here](). For simplicity i will just include a heading called page 2.

```# Page 2```

3. Now save the file. You'll notice some movement in the terminal. This is mkdocs automatically rebuilding the document since it has detected a change in the documentation. Now go an view the documentation in your browser. If you have already closed the browser just hold `ctrl` and click on the link in the terminal `http;//127.0.0.1:8000` to reopen the documentation in your browser.

You'll see that the navigational pane has changed and there is now a `Page 2` tab availible. 

![nav_pane_change]()

#### Navigation

What do we do if we want to add many pages to our documentation. If each page adds another page in the navigation then we will quickly run out of space for new pages. We can create a navigation pane to fix this problem. Two step are needed to create a proper navigation pane.

![too_many_files](no nav in mkdocs)

**First step:** We need to create a folder (or many) and move the markdown files into those folders.
**Second step:** We need to devine the navigational tree structure in the `mkdocs.yml` file so it knows which files to link. 

#### Why create folders
this is to orgenise pages according to the relevant sections

#### Setting-up the nav
We can change the layout of the nav by simply addign a few lines of code. This will make out interface look mauch better and make finding things you want to look for much easier. 

- #### How the it works
  By using a `nav` attribute in the `mkdocs.yml` config we can change the layout of the navigational pane and navigational toolbar. This helps a great deal id you have many markdown files you want to display, allowing us to sort the files into more manageable setions or group them together. 

  Inoredr to change our nav-bar we first need to specify that we want to create a custom nav. we can do this simply by adding the following to `mkdocs.yml`:

  ```nav:```

  ![mkdocs.yml_nav_added]()

  Once this is done we need to speficy the folder tree of the nav.

- #### Folder tree
The folder tree allows us to specify the exsact route you would want the documnets to be displayed in. Think of this like creating a menu wher you need to navigate to one directory and then to the next to see the content you want to view. THis all sound more complicated than it is. 

Inorder to set this up we need to understand how th mkdocs folder tree works
```
dir:
    |__ Menu 1:
    |     |__ Sub Menu 1:
    |           |__ File 1
    |           |__ File 2
    |     |__ Sub Menu 2:
    |           |__ File 1
    |           |__ File 2
    |            
    |__ Menu 2:
          |__ Sub Menu 1:
                |__ File 1
                |__ File 2
                |__ File 3
```

Mkdocs supports the following folder trees

To add a `nav` we should edit the `mkdocs.yml` file, and add the following to it:

```
nav:
        - Home: index.md
```

#### Explanaision of how it works

#### Styling limits:
Many other things can be specified in the config document and I strongly advise anyone to take some time to read through the documentation provided by mkdocs. The documentation provides indepth explanations of what features are affected and how things might change as well as displying the differnces through the use of examples. 

The documentation of mk docs can be accessed [here]()