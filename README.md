## Enforce every commit references a ticket

#### Setup
    git clone git://github.com/sartak/git-jira-ticket-msg.git

    ln -vis `pwd`/git-jira-ticket-msg/commit-msg My-Project/.git/hooks
    cd My-Project
    git config --add ii.project MYPROJ
    git config --add ii.project ALTPROJ

#### Hack hack hack...

    git commit -am 'test'
    *
    *
    *
    Aborted! Your commit message's first line must reference a ticket MYPROJ-### or ALTPROJ-###

    > git commit -am 'add widget MYPROJ-1'
    [master 981b439] add widget MYPROJ-1

#### Hack hack hack...

    > git commit -am 'fix gizmo ALTPROJ-5'
    [master 459ec03] fix gizmo ALTPROJ-5

