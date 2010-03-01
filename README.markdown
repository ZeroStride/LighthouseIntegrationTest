# Lighthouse Integration Test Repository
This repository is for testing our bugfix workflow integration with Lighthouse. It contains bugs which will be automatically re-initialized by the commits in the 'repush'.

### Repush
The 'repush' script first resets the local repository to the first commit, then force-pushes the repository to the origin. It then uses the functionality of the git reflog to easily return to the previous state of HEAD in the local repository, and force-pushes the repository to the origin. This allows for simple, consistent testing of the Lighthouse-workflow post-receive server.

### Lighthouse Test Project
This repository is wired in to this (public) [Lighthouse project](http://gameclay.lighthouseapp.com/projects/47141-workflow-test/)
TODO: Look another TODO!
### Bug Fix Syntax
When the post-receive hook sees a message in the format:
`Merged branch 'initials/bug-#'`
It should mark the corresponding bug as 'fixed'.
