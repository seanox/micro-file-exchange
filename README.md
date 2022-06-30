# Description
To use local files that are continuously synchronized over a network with several
computers and that almost in real time -- so the goal. 

Micro-File-Exchange is a small service for Windows that does this. Local
directories are declared as workspaces, to which directories on network drives
are assigned as repositories. 

Locally, a synchronized copy of the data from the repository is always used.
Therefore, it is not a problem if the repository is not available. Then the
synchronization pauses and resumes when the repository is available again.   

Managing changes and versions is a very complex issue, which was solved very
simply. Like in the local file system -- who writes last wins. There is no
merging and there are no locks.
