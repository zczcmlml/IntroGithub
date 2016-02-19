# Solve Permission Problem and Http 403 Error
- Cheng Zhang 02/19/2016
- The file works for users using github through ssh
- I just tried on Jay's machine using Putty
- Here, I use pcml repository as an example

### Http 403 Error
1. Go to the repository folder where contains .git folder

  ``` 
  $ cd YOUR_DIRECTORY/pcml
  ```
2. Open .git/config

  ```
  $ vi .git/config
  ```
  
3. Under `[remote "origin"]`, in the `url` part, change everything before `github.com` to `ssh://git@`

  ![edit .git/config](https://github.com/zczcmlml/IntroGithub/blob/master/cap_.git_config.PNG)
  
4. Save and quit

### Solve Permission Problem
1. 

