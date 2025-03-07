---
<<<<<<< HEAD
publish: true
title: ⌨️ Gh
tags:
  - shell
---
=======
{"publish":true,"title":"⌨️ Gh","tags":["shell"],"PassFrontmatter":true}
---

>>>>>>> f251504d101c483fe49b365b5a32e2a9e86c3726
### Fork a Repository Using GitHub CLI

1. **Install GitHub CLI**:
    
    - If you don't have the GitHub CLI installed, you can download and install it from the [GitHub CLI installation page](https://cli.github.com/).
2. **Authenticate**:
    
    - Authenticate with your GitHub account using the following command:
        
        sh
        

		 ```
        gh auth login
        ```
        
3. **Fork the Repository**:
    
    - Use the `gh repo fork` command followed by the repository you want to fork. For example, to fork the `octocat/Hello-World` repository:
        
        sh
        

		```
        gh repo fork octocat/Hello-World
        ```
        

### Example

sh

```
# Authenticate with GitHub
gh auth login

# Fork the repository
gh repo fork octocat/Hello-World
```

This will create a fork of the repository in your GitHub account. By default, the CLI will prompt you to choose whether to clone the forked repository to your local machine. You can accept or decline based on your preference.

### Additional Options

You can also specify additional options with the `gh repo fork` command. For example:

- `--clone`: Clone the fork after creating it.
- `--remote`: Add a remote for the fork.