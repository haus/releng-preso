!SLIDE bullets incremental
# Where we are #
## (Two months ago, circa Q1 2013) ##

* The same tasks between projects
* On commit package builds
* One release workflow
* Self-service packages for developers

!SLIDE bullets incremental
# Uniform Tasks #

* Run `rake package:tar` for a tar.
* Run `rake package:deb` for a deb.  
(wraps cowbuilder and pbuilder)
* Run `rake package:rpm` for an rpm.  
(wraps mock and rpmbuild)

!SLIDE bullets incremental
# One Workflow #

* Checkout the tag to ship
* Run `rake pl:jenkins:uber_build` (should automatically have happened via jenkins)
* Run `rake pl:jenkins:uber_ship`
* Get a beer
* Send a release announcement


!SLIDE bullets incremental
## Occasionally devs like using real packages ##
# That's awesome! But how do they get them? #
* Checkout the commit they want
* Run `rake pl:jenkins:uber_build` (should automatically have happened via jenkins)
* Run `rake pl:jenkins:retrieve`

!SLIDE bullets incremental
# Did that sound familiar? #
* (it should)
