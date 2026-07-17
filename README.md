# CS50 Week 4: Memory

Welcome to Week 4 of CS50! 

This repository is fully configured with a GitHub Codespace environment. You do not need to install anything on your computer to complete these problem sets—all coding, compiling, and testing can be done directly in your web browser.

## Step 0: Create a GitHub Account
If you don't already have a GitHub account, you must create one to use GitHub Codespaces:
1. Go to [https://github.com/signup](https://github.com/signup) and create a free account.
2. Make sure you are logged in before proceeding to the next step.

## Step 1: Launch Your Environment
1. Go to [www.codingrabbit.dev](https://www.codingrabbit.dev) and sign in with the email address and password assigned to you.
2. On the left tab, click **Codespace Launch**.
3. Find your section and click **Launch Codespace**.
4. At that point, you will be asked to sign into GitHub.
5. A new browser tab will open with a web-based version of VS Code. Please wait a minute or two for the environment to build.

## Step 2: Sign into Coding Rabbit
Our custom AI Teaching Assistant, **CodingRabbit**, is pre-installed in your environment to help you learn! 
1. Click **Sign In**. This will securely open a *new browser tab* and ask you to log into the course platform.
2. After logging in successfully, the page will display your temporary authorization code. Click the **Copy** button on the screen.
3. Switch back to your original **VS Code browser tab** and **Paste** the code into the prompt window at the top center of the screen to finish signing in.
4. You can now use CodingRabbit for **Homework Assist** (to debug your current code) or **Study Assist** (to explain complex concepts)!

## Step 3: Start Your Problem Sets
Inside this repository, you will find several problem set folders for Week 4:
* `volume/` - Write a program to scale the volume of an audio file.
* `filter-less/` - Apply basic photo filters to images. (Less comfortable version)
* `filter-more/` - Apply photo filters and edge detection to images. (More comfortable version)
* `recover/` - Recover deleted JPEG images from a raw memory card file.

**Note on Filter:** 
You only need to submit *one* of the filter assignments. Choose either `filter-less` (if you are feeling less comfortable) or `filter-more` (if you are feeling more comfortable).

Each folder contains a `README.md` with specific instructions and the exact terminal commands you need to get started (including the `curl` commands needed to download the distribution code for these assignments).
1. Use the **Explorer** icon (the file folders on the top left of your sidebar) to click into a problem directory and read its `README.md`.
2. Follow the instructions to download the starter code, write your C code, and begin working!
3. Click on the **Coding Rabbit** icon on the left of the screen anytime you need help.

## Step 4: Shutting Down (Important!)
GitHub gives you a limited number of free compute hours per month for Codespaces. If you simply close your browser tab, the Codespace stays running in the background for 30 minutes before timing out, draining your free hours!

When you are done working for the day, **always stop your Codespace**:
1. Open the VS Code Command Palette by pressing **`F1`** (or click the gear icon in the bottom left -> Command Palette).
2. Type **`Codespaces: Stop Current Codespace`** and hit Enter.
3. You can safely close the tab once the session ends.

*(Alternatively, you can manage and stop your active environments at [github.com/codespaces](https://github.com/codespaces))*

## Step 5: Saving & Submitting Your Work
Because you launched your Codespace from a template directly, your work is currently saved in an isolated, unpublished local repository inside the Codespace container. 

### How to Save Files
By default, VS Code will often auto-save your files. However, you can manually save any file by pressing **`Ctrl + S`** (Windows/Linux) or **`Cmd + S`** (Mac) on your keyboard, or by clicking **File > Save** in the top menu bar.

### How to Submit (VS Code Method)
To safely back up your code to a private repository on your GitHub account and submit your assignment:
1. Open the **Source Control** panel (the Git icon on the left sidebar in VS Code).
2. Hover over the word **Changes** and click the **`+`** icon to stage all your changed files.
3. Type a message in the text box (like "Finished assignment") and click the **Commit** button.
4. Finally, click the large blue **Publish Branch** button.
5. VS Code will prompt you to publish to a private repository on your GitHub account. Follow the prompts to confirm.

### How to Submit (Terminal Method - Optional)
If you prefer using the command line, you can achieve the exact same result by running these commands in the terminal at the bottom of the screen:
1. `git add .` *(stages all your changed files)*
2. `git commit -m "Finished assignment"` *(saves the changes to history)*
3. `git push` *(VS Code will intercept this and ask if you want to publish the branch to a private repo)*

Your code is now safely backed up and visible in your new private GitHub repository!

## Step 6 (Optional, Advanced): Update Your Environment
This repository's `.devcontainer` setup (the tools and CodingRabbit extension pre-installed in your Codespace) is occasionally updated after courses have already started. If you're comfortable with git and want to pull in the latest version without disturbing your own work, run these commands in the terminal:

1. `git remote add upstream https://github.com/emowat/codingrabbit-cs50-week4.git` *(one-time setup — links you to the original course repository; skip this if you've already done it once)*
2. `git fetch upstream`
3. `git checkout upstream/main -- .devcontainer` *(pulls in only the environment configuration — your own code is untouched)*

VS Code will detect that the environment configuration changed and prompt you to rebuild your container — click **Rebuild** when asked, and your environment will update in place. This shows up as a normal file change afterward, so it'll be included automatically the next time you save/submit your work (Step 5 above).
