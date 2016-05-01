**installing CSBtools on Ubuntu 14.04**

+ download jist-cruise 3.2: http://masijenkins.vuse.vanderbilt.edu:8080/job/Build%20JIST-CRUISE/mipav=%2Fshare%2Fhudson%2Fmipav-nightly/lastSuccessfulBuild/artifact/jars/JIST-CRUISE-2016Feb07-12-05PM.jar
+ download MIPAV 7.3.0: http://mipav.cit.nih.gov/download.php
+ download CBS tools 3.0.7: https://www.nitrc.org/frs/?group_id=606
+ install MIPAV to ~/mipav (set JAVA limit high, I used 8 GB)
+ `mkdir ~/mipav/plugins`
+ `cp` jist-cruise.jar and csb-tools.jar to `~/mipav/plugins`
+ open MIPAV
+ from the top menu bar, go to install plugins.
+ install jist-cruise and cbs-tools in order (note, cbs-tools will claim to have failed, but it actually installed everything).

**Running a CBS-tools pipeline**

+ open the JIST layout manager
+ open the desired pipeline from `~/mipav/plugins/layouts-r3.0/`
+ along the top (blue boxes), specify your inputs.
+ save this layout with a new name.
+ open the JIST Process Manager
+ load the saved layout.
+ under layout preferences, specify your output folder
+ NB: in some cases (I have no idea why) JIST fails to understand your output directory and will try to 
  dump the outputs into `/exp-0000`, and will immediately fail because you do not have write permissions.
  The easy (dumb) solution to this problem is to (assuming you have root access) link `/exp-0000` to a folder like
  `~/mipav-outpus`:

    mkdir ~/mipav-outputs
    sudo ln -s ~/mipav-outputs /exp-0000

+ finally, run the pipeline. You should see intermediate files appearing in `~/mipav-outputs`
 
