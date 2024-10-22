# Signals-And-Data-Autumn-2024
This repository contains the exercises for each week of the 02462 Signals and Data course at DTU for autumn 2024. 

## Set-up virtual environment
To use this repository most effectively, we recommend you set up a virtual environment. We provide two different general methods for configuring this virtual environment.

### Using Poetry and Conda (Reccommended)

*Poetry is (in this case) a much superior tool, as it effectively straightjackets you to use the same package versions as the authors of this material, we therefore recommend this as the package management tool of choice.*

*IMPORTANT: Do not do this in your base environment, it will fuck up the whole thing and be terrible. For God's and all our sakes, MAKE A NEW CONDA ENVIRONMENT!!!!*

<!-- *Based on how clean your existing conda installation is, **it should be impossible to fuck up*** -->

1. Create a new conda environment, open your terminal (or specific conda terminal): \
```conda create --name your_env_name```

2. Activate the new conda environment
```conda activate your_env_name```
 
3. Ensure pip is installed in this new conda environment
```conda install pip```

4. Install pipx using pip (needed to install poetry)
```pip install pipx```

5. Install poetry using pipx
```pipx install poetry```

6. Add the path to poetry to your given terminal
```pipx ensurepath```

7. Use poetry to install the packages of this course
```poetry install --no-root```

8. Profit


### Using Pip and Pip requirements (Basic)

*Using this method is **not** reccomended as it opens you up to possible version mismatches and errors down the line. We will not be held responsible for package mismatches that appear as a result of this*

0. (Optional): Clone this repository, open a terminal a write: \
  ```git clone https://github.com/02462-Signals-and-Data/Signals-and-Data-Autumn-2024-student.git```

1. Create a new conda environment, open your terminal (or specific conda terminal): \
 ```conda create --name your_env_name```

2. Activate your new conda environment by running
```conda activate your_env_name```

3. Ensure pip is installed in this new conda environment
```conda install pip```

4. Navigate to the folder with the requirements file and install them all using pip: \
```pip install -r requirements.txt``` 

1. Before running your code (in a notebook), be sure to:  
   1. Select your new environment as your Python interpreter (if using VSCode)
   2. Activate your environment by inputting ```conda acitvate your_env_name``` and open a jupyter notebook with ```jupyter notebook```

*Do remember to ask for help from your TAs, a chatbot or Google if you run into any problems performing the above steps.*

## Pulling updates

During the course, we will both upload new material durig the weeks, as well as occasionally update existing material. To access these new updates, simply navigate to your project repository, open a terminal and write:

```git pull --rebase --autostash```

This **should** automatically do the following:

1. Stash your saved changes to the exercises
2. Pull the remote changes while rebasing your version to be placed at the 'head' of the git history
3. Apply your stashed changes on top of these pulled changes.

**Warning:** This might cause problems if we have pushed changes to an exercise **after** you have made changes to it. In this case our new changes will either be overwritten by your local changes, or simply 'coexist' with your changes, meaning some code blocks might not make sense any longer. 

You are of course free to use your own methods of pulling and such, but using this method automatically stashes and reapplies your local changes. Meaning:

1. Git doesn't bitch about you not having commited or stashed your changes
2. Git does not overwrite your precious changes to existing weeks (in case we change something in the previous weeks to fix and error, for example)
3. **HOWEVER** in the case of 2. it *might* lead to merge conflicts and the like, as your local changes are applied willy-nilly on the remote changes.

