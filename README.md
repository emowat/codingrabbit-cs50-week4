# CS50 Week 4: Memory

Welcome to Week 4 of CS50! 

This repository is fully configured with a GitHub Codespace environment. You do not need to install anything on your computer to complete these problem sets—all coding, compiling, and testing can be done directly in your web browser.

## Step 1: Create a GitHub Account
To use GitHub Codespaces, you must have a GitHub account. If you do not have one:
1. Go to [https://github.com/signup](https://github.com/signup) and create a free account.
2. Make sure you are logged in before proceeding to the next step.

## Step 2: Launch Your Environment
1. Click the green **Use this template** button at the top right of this repository.
2. Select **Create a new repository** from the dropdown. 
3. Name your repository (e.g., `cs50-week4-YOURNAME`) and select **Private**. 
4. Click **Create repository**. 
5. Once your new private repository is created, click the green **Code** button, select the **Codespaces** tab, and click **Create codespace on main**.
6. A new browser tab will open with a web-based version of VS Code. Please wait a minute or two for the environment to build.

## Step 3: Sign into Coding Rabbit
Our custom AI Teaching Assistant, **CodingRabbit**, is pre-installed in your environment to help you learn! 
1. Click **Sign In**. This will securely open a *new browser tab* and ask you to log into the course platform.
2. After logging in successfully, the page will display your temporary authorization code. Click the **Copy** button on the screen.
3. Switch back to your original **VS Code browser tab** and **Paste** the code into the prompt window at the top center of the screen to finish signing in.
4. You can now use CodingRabbit for **Homework Assist** (to debug your current code) or **Study Assist** (to explain complex concepts)!

## Step 4: Start Your Problem Sets
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

## Step 5: Shutting Down (Important!)
GitHub gives you a limited number of free compute hours per month for Codespaces. If you simply close your browser tab, the Codespace stays running in the background for 30 minutes before timing out, draining your free hours!

When you are done working for the day, **always stop your Codespace**:
1. Open the VS Code Command Palette by pressing **`F1`** (or click the gear icon in the bottom left -> Command Palette).
2. Type **`Codespaces: Stop Current Codespace`** and hit Enter.
3. You can safely close the tab once the session ends.

*(Alternatively, you can manage and stop your active environments at [github.com/codespaces](https://github.com/codespaces))*

## Step 6: Saving & Submitting Your Work
While your Codespace saves files automatically, your work is **not** permanently backed up to your GitHub repository until you commit and push it. Codespaces are automatically deleted by GitHub if left inactive for 30 days!

To safely back up your code and submit your assignment, run these three commands in the terminal:
1. `git add .` *(stages all your changed files)*
2. `git commit -m "Finished assignment"` *(saves the changes to history)*
3. `git push` *(uploads the changes to your private repository)*

Your code is now safely submitted and visible in your repository!
