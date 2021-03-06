1.  Setup IDE to allow weka imports

2.  Code is included that breaks down training data into percentage increments, builds the classifier, and applies the classifier to a separate test set.  The results are output in a .dat file.

3.  You will need GNUPlot to plot the data.  It can be found at http://sourceforge.net/projects/gnuplot/?source=typ_redirect

4.  Run the code and it will generate .dat files for each algorithms training and test set for False negative rate and false positive rate.  In order for the code to work the data set must be in the same directory as the code class.  These .dat files can be plugged into GNUPlot.    

5.  In the GNUPlot cmd line cd to the directory containing the .dat files.   Enter the following command:

	plot 'TrainingFPR.dat' u 1:2 smooth bezier title "FPR Training Set",'TestFPR.dat' u 1:2 smooth bezier title "FPR Test Set",'TrainingFNR.dat' u 1:2 smooth bezier title "FNR Training Set" dashtype (20,20) linecolor rgbcolor "red",'TestFNR.dat' u 1:2 smooth bezier title "FNR Test Set" dashtype (20,20)
	
	where TrainingFPR.dat and TestFPR.dat are the names of your .dat files containing the false positive rates for the training and test sets for each algorithm.  TrainingFNR.dat and TestFNR.dat contain the false negative rates for each algorithm.
	
6.	The .dat files follow a naming convention.  The .dat files with the prefix ANN are the data generated by the Multilayer Perceptron.  Files with the prefix ADA conetain the data generated by the AdaBoost.  Files with the prefix DecTree contain the data generated by the J48 decision tree algorithm. Files with the prefix IBK contain the data generated by the nearest neighbors algorithm.  Files with the prefix SMO contain the data generated by the SVM algorithm using a PolyKernel.  Files with the prefix SMORBF contain the data generated by the SVM algorithm using the RBFKernel.  Files with the suffix Tic contain data belonging to the Tic Tac Toe data set.  Files without the suffix Tic belong to the Chess data set.
