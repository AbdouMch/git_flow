#Git workflow with release
--------------------------

### Branching

- Create develop branch
- push to remote
- For each new feature create a feature branch : for example  feature/first-feature : `git checkout -b feature/first-feature`
- Commit new code in the new branch and push to remote : `git push --set-upstream origin feature/first-feature`
- After validating the new dev and testing the feature, we add the new code to  the develop branch. 
- Rebase feature branch code into develop:
  - `git checkout feature/first-feature`
  - `git rebase development`
  - `git push origin feature/first-feature`
  - Create a pull request in the remote, rebase and merge the pull request
- Update the local development branch : `git pull origin develop`
- Delete the feature branch : 

  - delete locally : `git branch -d feature/first-feature`
  - delete in the remote repo if not deleted when merging : `git push origin --delete feature/first-feature`
- 