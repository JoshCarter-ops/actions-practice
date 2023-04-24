GitHub Actions

## Instructions

Here are some initial steps to get started:

**ONLY UBUNTU RUNNERS CAN BE USED - USE THIS FOR TESTING OUT NOT BUILDING!**

1.  Install Docker: [Docker Link (macos)](https://docs.docker.com/desktop/install/mac-install/)
    
2.  Install 'act':
    
    ```
    brew install act
    ```
    
3.  Clone the following Repository: [GitHub Actions Practice](https://github.com/JoshCarter-ops/actions-practice)
    
4.  Navigate to the new repository and run ‘**act**', if you have an Apple Silicon CPU run '**act --container-architecture linux/amd64**' this will take you through the setup process, I would select the lowest container to run to reserve your systems resources.
    
    ```
    # NON Silicon CPU's 
    act
    # Apple Silicon CPU - Consider adding this line in your ~/.actrc file
    --container-architecture linux/amd64
    ```
    
5.  Now you are set up you can do a few things:
    
    1.  Run an Action
        
    2.  List the possible actions to run
        
    3.  Branch off and create your own as practice
        
6.  To RUN an action you can use:
    
    ```
    act -j <Job ID>
    ```
    
7.  To LIST an action you can use:
    
    ```
    act -l
    ```
    
8.  If you plan on rerunning the action over and over, consider adding '-r' for reuse as to not the build the container over and over again.
    
    ```
    # To reuse the container it will look like this:
    act -j <Job ID> -r
    ```
    

**Please ensure that if you create a branch for this repo, delete it when you are done - we want to keep it as simple as possible.**
