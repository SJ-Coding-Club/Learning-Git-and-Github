# Learning-Git-and-Github
Use this repository to learn how to contribute to projects. This tutorial is from a Windows perspective but you should have a very similar experience on Linux or Mac. I will also be posting a video for you guys, which should be easier to follow.

### Creating a GitHub account
This is pretty straightforward, just sign up for GitHub. Note that if you are a senior going to college this fall, if you use your .edu email, you can get some neat bonuses from GitHub's [student developer pack](https://education.github.com/pack).

### Setting up Git
Git is a version control system that tracks changes made to code and makes it a lot easier for programmers to collaborate on the same set of files. 

#### Install Git
Before you install git, check if you already have it. Open up a command line / terminal and run the command ```git```. If it recognizes the command, move onto the next step.

Otherwise, you'll need to [download and install](https://git-scm.com/downloads) it locally on your computer, though it shouldn't take very long.

#### Forking this repository
Now that you have git, fork this repository by hitting the button on the top right labeled ```Fork``` and then select your account in the popup menu.

### Clone your forked repo
In your forked version of this repository, click the green ```Code``` dropdown button and copy the HTTPS link that appears to your clipboard.

Open up a command line / terminal and change your directory to somewhere you can easily access, like Desktop. This location may vary for your system, so be sure to ask me on Discord if you have any issues in finding an easily-accessible directory to clone into.

```bash
# Change into a directory you can easily access
cd desktop
```

Then, type ```git clone ``` hit space and then ```CTRL+V``` to paste the HTTPS link you copied from before.

It should look something like this, but with your username:
```
git clone https://github.com/YOUR_GITHUB_USERNAME/Learning-Git-and-Github.git
```

### Making changes to ```index.html```
Now, locate the folder you just cloned within your actual file explorer, not the cmd line.

Select ```index.html``` and open it with a text editor, or just open up Notepad and use File -> Open and locate index.html.

This is what you should see in ```index.html```:

```html
<!DOCTYPE html>
<html>
  <h1>Contributors:</h1>
  <li>Jack Donofrio was here.</li>
</html>
```
Since the time I wrote this, there may be more names, but that does not matter. Just add in a new ```<li>Name was here</li>``` right below the last set of ```<li>``` tags with your name.

This is what it should look like after you edit it:

```html
<!DOCTYPE html>
<html>
  <h1>Contributors:</h1>
  <li>Jack Donofrio was here.</li>
  <li>User9185 was here.<li>
</html>
```

Save the file and go back into the command line. Get back to the ```Desktop``` directory or wherever you decided to clone the repository.

Change your directory to the cloned repo using:

```bash
cd Learning-Git-and-Github
```

Next you will add the changes you made to ```index.html``` to the staging area. This basically is telling git that you will be including changes from this file to the next commit (A commit is the state of the project that will be recorded in the version history and will eventually show up on GitHub).

Add your changes using:

```bash
git add index.html
```

Now, you can commit these changes using:

```bash
git commit -m "Added my name to contributor list"
```

The -m piece just allows you to leave a commit message to describe what you just changed in a few words.

At this point, if this is your first time commiting to a git repository, you may have received an error telling you to identify yourself. If that happens, run the following commands with your GitHub email and username as the email and name:

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

Then try to run the same git commit command above again and it should work.

Finally, push the commands to your forked repository on GitHub using:

```bash
git push
```

At this point, it may ask you to authenticate yourself, so just select the browser option and sign into your GitHub account.

Finally, you can go to the online page for the repository you forked to your account, and there should be a ```Contribute``` button that drops down when you click it. Click that, select Open Pull Request, then Create Pull Request.

Once the pull request has been accepted by me or one of the other admins here, you should be able to see your name on the live website at https://sj-coding-club.github.io/Learning-Git-and-Github/

