---
layout: default
title: Jekyll training
navigation_weight: 1
---

# Jekyll training exercise

### Fork the repository to your personal account

Navigate to [Jekyll repo](https://github.com/maggima/jekyll) and hit the fork button.

<img src="/jekyll/assets/images/fork.png" width="400"/>

### Clone the repo locally

When it's forked to your personal Git account, clone it locally by pressing the green clone button and copy the address.

![clone](/jekyll/assets/images/clone.png)

### Add the main repository reference to the local repo

Open Git bash and go in the directory of the cloned repo and execute the following command :

```bash
git remote add upstream https://github.com/maggima/jekyll.git
```

### Add a Markdown page

Add a new markdown file under the `/pages/folder1/` folder. The file needs to have the .md extension.

Add at the top of the file those lines :

```
---
layout: left-menu
title: My New Page
order: 1
---
```

*Note : title and order can be changed so it reflects in the side menu*

The new file must be added to the Git index so it's sent when commiting and pushing changes.

```bash
git add [file-name].md
```

### Commit and push your changes remotely

```bash
git commit -m "I added my first page"
```

```bash
git push origin master
```

### Go on your Github repository and create a Pull Request

Create a pull request by pressing the New Pull Request button and add some comments describing what has changed. A maintainer from the main repository will then review your changes and then will accept or not the changes to be integrated into the main repository.

When the Pull Request has been accepted or other changes happened to the main repository (always good to do before starting to work every day), you need to fetch the remote changes locally.

```bash
git fetch upstream
```

```bash
git rebase upstream/master
```

