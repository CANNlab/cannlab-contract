**setup**

+ environment set-up through the `source.me` file. remember to edit the path.
+ to load environment: `source source.me`


**bin**

+ contains one-off scripts used to get the raw data ready for epitome.

**demographics**

+ a copy of the raw demographics data.

**epitome**

+ a clone of the version of epitome used to analyze the data.

**epitome-data**

+ the epitome data folder, containing all intermediate steps, some qc, and helper scripts.

**output**

+ the nonlinear-registered to MNI space outputs of epitome, ready to analyze.

**raw**

+ the raw data. also contains the fieldmap-unwarping steps (see bin/).

**reference**

+ papers and notes related to the data.

**working**

+ copies of the data from raw/ used to run to cbs-tools, which was used to compute the anatomical brain masks (for the MP2RAGE data).

**freesurfer**

+ downsampled and deskulled versions of the files found in working/ were run through freesurfer here.
+ see the script in bin/ for more details.
