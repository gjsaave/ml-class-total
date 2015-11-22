1.  BURLAP was used for this assignment.  Download it from https://github.com/jmacglashan/burlap

2.  A few files in BURLAP were modified to allow the graphs to be made.  The classes modified are ValueIteration and PolicyIteration.  

3.  ExampleGridWorld was modified and has been included.  You can use this class to generate all the results and graphs shown in the analysis.  The small grid world is set as default.  If you want to use the large grid world comment out lines 61-71 and uncomment ...


4.  You will need GNUPlot to plot the data.  It can be found at http://sourceforge.net/projects/gnuplot/?source=typ_redirect

5.  Run the code and it will generate .dat files for each algorithms training and test set for False negative rate and false positive rate.  In order for the code to work the data sets must be in the same directory as the code class.  These .dat files can be plugged into GNUPlot.



 6.  In GNUPlot make sure the terminal type is set to 'wxt'.  There should be a message output on startup informing you of your terminal type. In the GNUPlot cmd line cd to the directory containing the .dat files.   Enter the following commands:
 
 plot 'VIIter.dat' u 1:2 smooth bezier title "VI",'PIIter.dat' u 1:2 smooth bezier title "PI"

 plot 'VITime.dat' u 1:2 smooth bezier title "VI",'PITime.dat' u 1:2 smooth bezier title "PI"
 
	The first command will plot the iterations graph and the second command will plot the time graph.