1.  Setup IDE to allow weka imports.  I used Eclipse.  If you want to allow weka imports you must add them to the java build path under preferences.  Or you can use the command line, in which case, you'll need to add the weka api to your class path.  You will also need the jars necessary to import Java.io and java.net.URL .  You must also import the StudentFilters package.  The jar is included with my submission.  

2.  To create cluster plots:  Open the data set in Weka Explorer then go the cluster tab.  Choose the algorithm you want and after it is done running rights click on the text result in the bottom left window.  From here choose visualize cluster assignments.


5.  In GNUPlot make sure the terminal type is set to 'wxt'.  There should be a message output on startup informing you of your terminal type. In the GNUPlot cmd line cd to the directory containing the .dat files.   Enter the following command:

	plot 'ANNTrainingXX.dat' u 1:2 smooth bezier title "Training Set",'ANNTestXXX.dat' u 1:2 smooth bezier title "Test Set",'ANNTrainingXXX.dat' u 1:2 smooth bezier title "Training Set" dashtype (20,20) linecolor rgbcolor "red",'ANNTestXXX.dat' u 1:2 smooth bezier title "Test Set" dashtype (20,20)
	
	where ANNTrainingXXX.dat and ANNTestXXX.dat are the names of your .dat files containing the error rates.  Replace the XXX with PCA, ICA, RP, or TPP for part 4.  For part 5 replace XXX with EM or KMeans if you want the error vs k graphs.  Use EMLC or KMeansLC as the suffix if you want the learning curves for the clusters as a feature.  