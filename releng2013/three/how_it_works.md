!SLIDE bullets incremental
# How It Works #


* On Jenkins, one job to build them all!
* * NodeLabelParameter plugin picks the right builder for the job
* * Slave clones git-bundle upload and git clones packaging
* * Execute build task
* * Send artifacts to distribution server

!SLIDE bullets incremental
## Previously, On the client side.. ##

* * Clone packaging repo (`rake package:bootstrap`) and package (`rake package:deb`)
* * Trigger build, sending git-bundle, build data file, sha, build type
* Note jenkins job url and go get a beer

!SLIDE bullets incremental
# Wait, this is awesome why? #

* * Jenkins job completely abstracted from project and target platform
* * Add new projects with zero jenkins-side maintenance
* * Scale by just adding more builders as Jenkins slaves, no reconfiguration
* * Commit does not need to be checked into upstream (do your worst)
