# lab_workflow_mock
Demoing how we can work with labs and answers using Git

### Restart all the work
This will reset the entire lab to the starting point
```sh
git reset --hard origin/main
```

### Get the answer for backend (only)
This will grab the answer for the backend only and overwrite any code the user has in the folder.
```sh
git checkout answer -- backend 
```
If there are new files that the user wants to clean out also, we can run the clean command
```sh
git clean -f -- backend
```
Neither of these will affect whatever changes have been done in the `/frontend` directory

### Get the answer for frontend (only)
This will grab the answer for the fronten only and overwrite any code the user has in the folder.
```sh
git checkout answer -- frontend 
```
If there are new files that the user wants to clean out also, we can run the clean command
```sh
git clean -f -- frontend
```

And here is how we can add a nice collapsible block at the end of each step with instructions on how to grab that specific step answer key:

<details>
  <summary>Need help with this step?</summary>
  
  You can set your entire backend folder to the current step by running a git command to grab it from the repo

  ```sh
git checkout tags/4.4 -b answer -- backend
```
</details>
