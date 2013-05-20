!SLIDE bullets incremental

## On Jenkins, one job to build them all! ##
* * NodeLabelParameter plugin picks the right builder for the job
* * Slave clones project and packaging repo
* Release the Hounds!
* (I mean...Execute the build!)
* * Send artifacts to distribution server
* * Jenkins wipes sweat from his brow and grabs us a beer

!SLIDE bullets incremental
## Previously, On the client side... ##

* * Clone packaging repo (`rake package:bootstrap`) and package (`rake package:deb`)
* * Packaging sends your project and build data to Jenkins
* * After a hard day's work, note the Jenkins job url and go get a beer

!SLIDE bullets incremental
# Wait, this is awesome why? #

* * Jenkins job completely abstracted from project and target platform
* * Add new projects with zero jenkins-side maintenance
* * Scale by just adding more builders as Jenkins slaves, no reconfiguration
* * Commit does not need to be checked into upstream (do your worst)
