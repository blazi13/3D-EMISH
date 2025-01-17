Image processing and analyzing code for chromatin structures in electron microscopy images.

Files:
 
denoiseTiff.py -removes unspecific noise from the EM tiff stack
denoiseSettings.py- configuration file for denoiseTiff.py
AnalyzeStructure.py- analises EMISH signal- alignes structure in principle axis coordinates, calculates mass centers and
segments domains
AnalysisParameters.py- configuration file for AnalyzeStructure.py
get_gradient (.cpp and .pyd)- auxialiry files 
SegmentDomain-auxialiry file

Requirements: Python2.7 with data science packages (tested using Anaconda with Python 2.7.14 under Windows10)
If the working directory is not in python library path, copy the file get_gradient.pyd into the library path.
For other systems (e.g. Linux) get_gradient.cpp has to be compiled. Execution time denoiseSettings.py~ 30 sec. AnalyzeStructure.py ~ 10 mins. for a single example 

Usage:
1. Set correct paths (including input file name /three dimensional tiff/) and options in denoiseSettings.py
2. Run python denoiseTiff.py to remove unspecific background
3. Set correct paths (including input file name with segmented structure) and options in 
4. Run python AnalyzeStructure to center and align it in princliple axis coordinate system, 
to determine local density centers and to segment it into domains.

The description of adjustable parameters given in files AnalysisParameters.py and denoiseSettings.py

Developed by Blazej Ruszczycki, 2019, e-mail:b.ruszczycki@nencki.gov.pl

Codes are compressed and packaged with zip file format, and split the file with 25Mb size using linux split commend.
After download four files (scripts_for_emish.zipaa, scripts_for_emish.zipab, scripts_for_emish.zipac, scripts_for_emish.zipad), please use the following linux commend to merge: "cat scripts_for_emish.zip* > scripts_for_emish.zip". 
Then, uncompress the zip file. 
