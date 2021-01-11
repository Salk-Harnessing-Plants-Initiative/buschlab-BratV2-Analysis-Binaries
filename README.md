# BRAT V2 Analysis Binaries
These are the binaries for BRAT V2 Analysis, a plugin that is ostensibly equivalent to the BRAT V2 plugin (plugin 1 of the BRAT pipeline) 
except skips the segmentation part and only does the analysis part (whereas the full BRAT V2 does both the segmentation and analysis). 
This is is intended to co-opt the BRAT pipeline with the new DeepBRAT project, which uses deep learning to do a better job of the segmentation than BRAT,
among other things.

# Notes by Christian G
This is implemented as a Fiji plugin. For installation, copy the brat_analysis-3.0.0.jar to your Fiji plugins folder.

There is also a dependency for the jung-algorithms jar. I'll also attach this file. Please copy the jung-algorithms-2.0.1.jar to your Fiji.app/jars folder.
Everything else should be covered by a Fiji default installation.

After installation, you'll find the "Brat Analysis" tool in your Plugin-menu. A GUI will open, if you click the Brat menu entry. Most of the parameters should be self explanatory. The default options fit the requirements of the sample images I got from Linjing (e.g. crop region, segmentation labels, ...), though I had to adopt the crop region for flipped images. There is now also the possibility to import a new plate layout (press the "+" button at the Advanced Options pane). This will import a list of Point ROIs, which has before been saved in Fiji (zip file). (The number of Point ROIs must exactly match the required number of positions (e.g. 24 for a 2x12 layout)). A new layout should be created on one of the original scans (including the gray border).
The output is a text file (besides the diagnostic images), which could be read by the BRAT Evaluation tool.
