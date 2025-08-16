\# MultiVersionSafe



This method of maintaining multiple game versions assumes that all edits on the latest main branch are designed for all versions, and edits on a version branch are specific to that version. It is possible to sync changes from a version branch but it is a little more complicated, requiring the commits to be moved to main. The only permanent downside of this method is that version branches will count every merge commit in "This branch is xxx commits ahead of main."



* Commit
* Commit
* Commit



New version is released



* Bump commit
* Create version branch
* Switch to version branch
* Revert bump commit
* Switch to main branch
* Commit
* Commit
* Commit
* Switch to version branch
* Merge from main branch
* Switch to main branch
* Commit
* Commit
* Commit



Compiler option for version is needed



* Switch to main branch
* Add BUILD\_FOR\_MAIN
* Commit
* Switch to version branch
* Merge from main branch
* Fix conflicts
* Commit the merge
* Write BUILD\_FOR\_VERSION
* Commit
* Switch to main branch



Need to update from version branch



* Switch to version branch
* Commit hashA
* Commit hashB
* Commit hashC
* Switch to main branch
* Cherry-pick hashA~..hashC (will duplicate the commits, but there's only a few)
* Switch to version branch
* Merge from main branch



Need to update from version branch without leaving duplicate commits



* Switch to version branch
* Commit hashA
* Commit hashB
* Commit hashC
* Switch to main branch
* Cherry-pick hashA~..hashC (creates duplicates)
* Switch to version branch
* Reset hashA~1
* Restore . (all)
* Merge from main



Need to make the same update to build files in each version branch



* Done by default



Need to make a specific update to build files on main version branch



* Make the change in main, then merge and revert on each version branch
