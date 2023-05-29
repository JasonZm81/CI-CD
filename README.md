## _Steps to automate deployment using GitHub Actions pipeline:_

#### 1.	Make sure database are all backup onto Magento.

#### 2.	Make sure to push/merge the new code changes into the specific branch.

#### 3.	Pull the latest code from the specific GitHub branch.
```sh
git pull origin <branch> 
```
For example,
```sh
git pull origin Integration2
```
#
#### 4.	 Create tag to trigger pipeline. 
#
##### 4.1  Assign git tagging. 
#

```sh
using git tag <tag-name> <commit-SHA>
```
For example,
```sh
git tag release/Integration2/application/v0.0.1 ab323ff62d1095ed203f42dd9e327b07c2343ea7 
```
#
##### 4.2 Git push the tagging.
#
```sh
git push origin <tag-name>
```
For example,
```sh
git push origin release/Integration2/application/v0.0.1
```
May refer to this website for more information: https://www.shellhacks.com/git-create-tag-push-tag-to-remote/ 
#
#### 5. Check the pipeline status on GitHub Actions. 
May refer to https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/viewing-workflow-run-history 
#
#### 6. Verify the application deployed onto Magento
#
#
#

