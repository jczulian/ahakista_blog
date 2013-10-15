


You just need to push an 'empty' reference to the remote tag name:

git push origin :tagname

Or, more expressively, use the --delete option:

git push --delete origin tagname

Pushing a branch, tag, or other ref to a remote repository involves specifying "push where, what source, what destination?"

git push where-to-push source-ref:destination-ref

A real world example where you push your master branch to the origin's master branch is:

git push origin refs/heads/master:refs/heads/master

Which because of default paths, can be shortened to:

git push origin master:master

Tags work the same way:

git push refs/tags/release-1.0:refs/tags/release-1.0

By omitting the source ref (the part before the colon), you push 'nothing' to the destination, deleting the ref on the remote end.
