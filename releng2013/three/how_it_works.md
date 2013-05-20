!SLIDE
# How It Works #

!SLIDE bullets incremental
## On Jenkins we have one parameterized job to build _all\_the\_things_ ##

* NodeLabelParameter plugin picks the right builder
* Slave clones git-bundle upload and git clones packaging
* Execute build task
* Send artifacts to distribution server

!SLIDE bullets incremental
## On the client side (a clone of a Puppet Labs project) ##

* Clone packaging repo (`rake package:bootstrap`) and rake your package of choice
* Trigger build, sending git-bundle, build data file, sha, build type
* Grab the jenkins job url and go get a beer

!SLIDE bullets incremental
# Wait, this is awesome why? #

* Jenkins job completely abstracted from project and target platform
* Add new projects with zero jenkins-side maintenance
* Scale by just adding more builders as Jenkins slaves, no reconfiguration
* Commit does not need to be checked into upstream (do your worst)
