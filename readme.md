MultiVersionSafe



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



Need to update from version branch without leaving duplicates



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
