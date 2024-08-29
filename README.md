# 🚀 Creating and Working with Two Branches in VS Code & AWS CodeCommit 🎨

## Overview

This guide provides step-by-step instructions on how to create and work with multiple branches in a Git repository using Visual Studio Code (VS Code) and AWS CodeCommit. You'll learn how to manage your code changes effectively, enabling better version control and collaboration. 🔄


![Animation](https://github.com/user-attachments/assets/b13e6ce9-a208-404e-842c-5377a379f904)

## Objective

🎯 **Learn & Apply** Git branching techniques with:
- 🛠️ **VS Code**: Work seamlessly with your branches
- 📁 **AWS CodeCommit**: Manage your repository and branches on AWS
- 👨‍💻 **Git**: Master the basics of branching and merging

## Prerequisites

Before starting, ensure you have the following installed and configured:
- **Visual Studio Code (VS Code)**: [Download VS Code](https://code.visualstudio.com/)
- **Git**: [Install Git](https://github.com/git-for-windows/git/releases/download/v2.46.0.windows.1/Git-2.46.0-64-bit.exe)
- **AWS CLI**: [Install AWS CLI](https://awscli.amazonaws.com/AWSCLIV2.msi)
- **AWS CodeCommit Repository**: Already created in your AWS account

## Steps to Follow

### 1. Clone the AWS CodeCommit Repository in VS Code

- Open VS Code and launch the terminal (`Ctrl + `` or View > Terminal`).
- Clone the repository using the command:
  ```bash
  git clone https://git-codecommit.<region>.amazonaws.com/v1/repos/<repository-name>
  ```
- Navigate to the repository directory:
  ```bash
  cd <repository-name>
  ```

### 2. Create the First Branch

- Create and switch to a new branch named `developer1`:
  ```bash
  git checkout -b developer1
  ```
- You're now working on the `developer1` branch. 🎨

### 3. Make Changes and Commit to the First Branch

- Edit your files in VS Code.
- Save your changes (`Ctrl + S`).
- Stage the changes:
  ```bash
  git add .
  ```
- Commit the changes:
  ```bash
  git commit -m "Add changes in developer1"
  ```

### 4. Push the First Branch to AWS CodeCommit

- Push the `developer1` branch to AWS CodeCommit:
  ```bash
  git push origin developer1
  ```

### 5. Create the Second Branch

- Switch back to the `master` branch:
  ```bash
  git checkout master
  ```
- Create and switch to a new branch named `developer2`:
  ```bash
  git checkout -b developer2
  ```

### 6. Make Changes and Commit to the Second Branch

- Make different changes for the `developer2` branch in VS Code.
- Save your changes (`Ctrl + S`).
- Stage the changes:
  ```bash
  git add .
  ```
- Commit the changes:
  ```bash
  git commit -m "developer2 code"
  ```

### 7. Push the Second Branch to AWS CodeCommit

- Push the `developer2` branch to AWS CodeCommit:
  ```bash
  git push origin developer2
  ```

### 8. Check the Current Working Branch

- Verify the current branch in VS Code by looking at the status bar at the bottom left.
- Alternatively, run the command in the terminal:
  ```bash
  git branch
  ```

### 9. Switch Between Branches

- To switch between `developer1` and `developer2` branches, use:
  ```bash
  git checkout developer1
  git checkout developer2
  ```

### 10. Merge the Branches (Optional)

- If you want to merge `developer1` into `master`:
  ```bash
  git checkout master
  git merge developer1
  ```
- Push the merged changes to AWS CodeCommit:
  ```bash
  git push origin master
  ```

## Conclusion

By following this guide, you can efficiently manage and work with multiple branches in VS Code while leveraging AWS CodeCommit for version control. This process is crucial for maintaining a clean and organized codebase, enhancing collaboration, and ensuring smooth project development. 🌟

