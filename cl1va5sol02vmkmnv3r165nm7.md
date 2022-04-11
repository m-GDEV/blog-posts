## How to publish a Hugo site on Github Pages

### Pre-requisites

- Github Account
- Basic command line familiarity
- A **Linux or Mac OS** machine (the github portion of this guide will work on windows but the command line commands may differ)
- A Hugo site

### Important Links

- <https://github.com>
- <https://github.com/git-guides/>
- <https://gohugo.io>

## Before we start

It is important to define some of the things we are going to be working with today. Let's have a look.

**Git** is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows (thousands of parallel branches running on different systems). [Wikipedia](https://en.wikipedia.org/wiki/Git)

**GitHub**, Inc. is a provider of Internet hosting for software development and version control using Git. It offers the distributed version control and source code management (SCM) functionality of Git, plus its own features. It provides access control and several collaboration features such as bug tracking, feature requests, task management, continuous integration and wikis for every project. Headquartered in California, it has been a subsidiary of Microsoft since 2018. [Wikepedia](https://en.wikipedia.org/wiki/GitHub)

**Hugo** is the world’s fastest static website engine. It’s written in Go (aka Golang) and developed by bep, spf13 and friends. [gohugo.io](https://gohugo.io/documentation/)

## Make a new repository on github

1. Go to your dashboard page on github. The URL should look something like **https://github.com/[USERNAME]**

2. Hover over the plus icon on the top right of the page and click **New Repository**
   ![new repository github](https://i.imgur.com/7CzvU3Z.png)

3. Create the repository
   - Name it whatever you like
   - You can make it **public or private**, but keep in mind your site will be public!
   - And then click create (don't worry about the other options)

## Get your Hugo files in order

- Make all neccesary changes you need to make to your hugo files. Your content, config etc.
- Then make **a new folder** with the same name as the repository you just made.
- **Copy / Move** you hugo files into the new folder

## Build the site and setup the repository in the terminal

If you have **not installed** git yet, search online for a tutorial. To verify it is properly installed, open up a terminal and type in `git --version`. It should display a version number; if not, then it is not properly installed.

- Open up a terminal and navigate to the folder you created with the `cd` command.
- Copy and run the follwing commands **line-by-line**
```bash
    echo "# My new Hugo Site!" >> README.md
    # This creates a file that describes your project!
    hugo
    # This will build your hugo site in this directory
    mv public docs
    # Necessary to change name of public folder when using github pages
    git init
    # This initializes a git repository
    git add -A
    # This adds all of your files to a commit
    git commit -m "Initial commit"
    # This commits all of the files you added
    git remote add origin https://github.com/[YOUR USERNAME]/[REPOSITORY NAME].git
    # This tells git that you want to push your files to this repository
    # from now on (make sure you replace your username into the URL)
    git push -u origin master
    # This pushes the files you just commited to the github servers
```

## Use github pages to host your site online

Go to your repository's page on github.

- Next, click on the settings section in the top centre of the page. It should look like this:
  ![settings panel github](https://i.imgur.com/z3hh8EI.png)
- Click the pages section on the left sidebar
- Select the `docs` folder from the dropdown and click save.
- Now go back to the repository page and you should see an **Environments** section on the page. Click it and press view deployment.
- If it shows a **404 error**, wait a few minutes a trying again (github is in the process of deploying the site)

## Congratulations! You have sucessfully hosted your hugo site on github.

**Today you have learned how to:**

- Build your hugo site and initialize a git repository
- Push the repository to github's servers
- Host the site using github using the files you pushed

Congrats! You just uploaded you files to github. You can view them by going to **https://github.com/[YOUR USERNAME]/[REPOSITORY NAME]** 