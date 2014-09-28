#Learning 3D computer graphics in OpenGL

- A series of examples each as a git branch

- Build Status of master branch - ![masterBranchBuildStatus](https://travis-ci.org/shearer12345/graphics_examples_in_git_branches.svg?branch=master)

##Branches available

- baseBuildWithNoFeatures
- baseBuildWithNoFeaturesWithTravisTesting
- master 

##Dependencies

- git
- premake4 (already in the repository for Windows)
- a build environment
    - Linux:
        - ```sudo apt-get install build-essential```
    - Windows:
        - Visual Studio, or something else of your choice
  
##Getting the code

- you'll need to recursively clone to repository, then make sure you pull all the branches and tags locally
    - on Windows, start Git Shell, then type bash to start bash
    - on Linux, just use bash (or another shell)

###Clone
```bash
git clone --recursive https://github.com/shearer12345/graphics_examples_in_git_branches.git
```

###Change in the directory
```bash
cd graphics_examples_in_git_branches
```

###pull and update all branches
```bash
for remote in `git branch -r `; do git branch --track $remote; done
```

###to update existing branches
```bash
for remote in `git branch -r `; do git checkout $remote ; git pull; done
```

##Usage

- For each example, you'll need to check out its branch
    - you can also **diff** between branches to see what's changed

- the cpp main function is consistently in the file main.cpp

- run premake4 to build the build files for your platform / build tool of choice
  - e.g. "premake4 gmake"  or "premake4 vs2010"

- build using your tool of choice
  - e.g. "make", or load in visual studio and build
  
- run the create exe (named after the branch)
  - e.g. "./baseBuildWithNoFeatures.exe"
  - or from Visual Studio
  
