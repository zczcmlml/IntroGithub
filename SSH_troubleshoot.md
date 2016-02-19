# Solve Permission Problem and Http 403 Error
- Cheng Zhang 02/19/2016
- The file works for users using github through ssh
- I just tried on Jay's machine using Putty. It probably is not a universal solution.
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

### Solve Permission Denied Problem (publickey)

1. Look at your SSH pubkey
  
  ```
  cat ~/.ssh/id_rsa.pub
  ```
  
  ![show ssh pubkey](https://github.com/zczcmlml/IntroGithub/blob/master/cap_cat_key.PNG)

2. If the pubkey does show up, skip this step

  Follow the Github Help: 
  [Generate a new SSH key](https://help.github.com/articles/generating-a-new-ssh-key/)
  
  And look at your SSH pubkey again

3. Follow the Github Help:
  [Adding a new SSH key to your Github account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

4. Now try the `git push` command 
