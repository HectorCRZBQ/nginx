# My Personal Webpage
This page was made with [**mkdocs**](https://www.mkdocs.org/) and [**virtual enviroment**](https://docs.python.org/es/3/library/venv.html)

## Content
 - [Home](https://github.com/HectorCRZBQ/Hector.github.io/blob/main/docs/index.md): Introduction and links to other sections.
- [Projects](https://github.com/HectorCRZBQ/Hector.github.io/blob/main/docs/projects.md): Featured projects I've worked on.
- [About Me](https://github.com/HectorCRZBQ/Hector.github.io/blob/main/docs/about.md): Information about my education, skills, and hobbies.
- [Contact](https://github.com/HectorCRZBQ/Hector.github.io/blob/main/docs/contact.md): Details on how to reach me.

## The 4 branches
 - *main* : the main brach of the project.
 - *develop* : the branch that conects main to feature.
 - *feature* : the main work branch were we upgrade our code
 - *gh-deploy* : used to deploy the local project using [Github Pages](https://www.mkdocs.org/user-guide/deploying-your-docs/).

# Why use a vitual enviroment?
To install there all the different libraries that we will use. This allows only to post on the repository the necesary code. 

# How to install **virtual enviroment**
1. We need to be on **Windows PowerShell on Administrator**
2. Execute the command **pip install virtualenv** to install the virtual enviroment
3. To create the enviroment we execute **python -m venv virtual_enviroment**
4. To activate the virtual enviroment we execute **virtual_enviroment\Scripts\activate**
5. To turn off the virtual enviroment we only need to execute **deactivate**

**<span style="color:red">IMPORTANT</span>** - Create a **.gitignore** to prevent uploading the virtual environment information to the repository.
1. Open the [Git Bash](https://git-scm.com/) 
1. Execute the command **nano .gitignore** and add the name of your virtual enviroment
2. Add inside the archive the name of the enviroment between bars "/name/", like */virtual_enviroment/*

# Why use mkdocs?
If you have no experience on doing web pages this is a pretty good option, you create a bunch of readme's and you deploy it on [github pages](https://www.mkdocs.org/user-guide/deploying-your-docs/)., this makes you all the different parts of the webpage (HTML, JS, CSS, ...) automatically.
   
# How to install **mkdocks**
**<span style="color:red">REQUIREMENT</span>** - We need to have installed the virtual enviroment to install the mkdocs
1. Inside the Windows PowerShell (Administrator) on the virtual enviroment that we created before we execute **pip install mkdocs**
2. We create a different folder than the virtual enviroment for the webpage
3. Inside the [**Git Bash**](https://git-scm.com/) we create a new mkdocs with the command **mkdocs new .**
4. After we execute this command it creates a **mkdocs.yml** that is like a index with all the different readme's that we created and on the begining it only links to the index.md, and also a folder by the name **docs** that contains only at the beginning the **index.md**.
5. To create a new readme or to update the mkdocs.yml we use the command **nano**, like *nano contents.md* or *nano mkdocs.yml*. To save we use Ctrl + X and later Y to confirm the changes.
6. To be abble to visualize the web page on the **virtual enviroment** we execute the command **mkdocs serve**
7. It will responds us with a link similar to *http://127.0.0.1:8000/* that is a local link, we put this inside a web browser and we have visual display of the webpage.

# **One Step Further**
1. You can use [Github Pages Deploy Command:](https://www.mkdocs.org/user-guide/deploying-your-docs/) **mkdocs gh-deploy** inside the Git Bash.
2. This creates a new branch with all the HTML, JS, CSS, ... and this allows us to turn off the virtual enviroment and access by a link like *https://**username**.github.io/**repository_name**/*, on this case is [https://hectorcrzbq.github.io/webpage/](https://hectorcrzbq.github.io/webpage/) that allows access using the servers of github pages

# Contact Sources
<div align="center">
  <a href="https://www.linkedin.com/in/h%C3%A9ctor-de-la-cruz-baquero-ba193429b/" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="52" height="40" alt="linkedin logo"  />
  </a>
  <a href="https://www.instagram.com/hector.baq/" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/instagram/default.svg" width="52" height="40" alt="instagram logo"  />
  </a>
</div>

# My Other webpage
The link to my other [webpage](https://hectorcrzbq.github.io/)
