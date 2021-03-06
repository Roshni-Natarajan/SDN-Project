
Project Review
=====================================================

Please fill in your name and net ID in the table below.

Lab Assignment       | Project Review
-------------------- | --------------------------------
Name                 | Roshni Natarajan 	
Net ID               | rn979@nyu.edu
Assigned project (#) | 16
Review due           | Monday, 4 May 11:59PM


## Overview

**1) Briefly summarize the experiment in this project.**

Summary of the experiment : 
	
1. A network environment having the topology of 6 Routers, a Client and a Server is first set up using the resources from GENI.

2. XORP is installed and used for implementing OSPF in all the Routers. 

3. Data Transfer Rate and Throughput are measured using iperf by varying the Delay(100ms, 200ms and 300ms) in three different scenarios :
	* When all the links are functional.
	* When one link is down.
	* When two links are down.

4. Step 3 is done for TCP and UDP. 

5. The Data Transfer Rate and Throughput are Plotted against Delay using an R script. 




**2) Does the project generally follow the guidelines and parameters we have 
learned in class?** 

The guidelines and Parameters learnt in class are not entirely followed. Details are provided below : 
			
1.Goal is stated properly. 

2.Metrics could have included Loss Rate in order to have accurate and detailed comparisons. 

3.Chosen parameters are fine.

4.Plan evaluation : Involves noting down the Data Transfer Rate measurements from the Server VM manually to process the R script. All the required Data should have been generated by some software process. 

5.Results obtained are plotted using Bar Plots which do not indicate any confidence intervals 




## Experiment design

**1) What is the goal of this experiment? Is it a focused, specific goal?
Is it useful and likely to have interesting results?**

Goal : 

In oder to analyse the performance of Transport Layer Protocols TCP and UDP in terms of Data Transmission Rate and Throughput on a Network implementing OSPF Routing Protocol by varying the Link Latency and by bringing down links (0 to 2 links) on the path.

It is a focused, specific goal as it is not biased and it specifically states :

1. the Environment where the experiment is conducted ( Network implementing OSPF Routing Protocol)
2. the performance that is being measured ( Data Transfer Rate and Throughput )
3. the parameters ( Delay and number of links down) that are being varied in order to measure the mentioned metrics. 
 
Useful and interesting results : 

Scenario of bringing down a few links could yield useful and interesting results. 
	
But, it is well known that UDP is used for Delay sensitive applications whereas TCP is used for Loss sensitive applications. Therefore, the scenario where the results are obtained by varying the delay might not classify itself as useful and interesting. 


**2) Are the metric(s) and parameters chosen appropriate for this 
experiment goal? Does the experiment design clearly support the experiment goal?**

Parameters chosen : 
	
Yes, the parameters chosen are appropriate for this experiment goal. They could have included Buffer Size as a parameter too.

Metrics chosen :

Data Transfer Rate and Throughput are similar metrics.

Yes, it does support the stated goal. 


**3) Is the experiment well designed to obtain maximum information with the 
minimum number of trials?**

The experiment involves significant effort as there are quite a number of scenarios considered. Also,there is only one trial per scenario which, if increased, would result in more effort.


**4) Are the metrics selected for study the *right* metrics? Are they clear, 
unambiguous, and likely to lead to correct conclusions? Are there other 
metrics that might have been better suited for this experiment?**

Yes, the metrics selected are good metrics because they clear and unambiguous and lead to correct conclusions . 
They could have included Loss Rate in order to have accurate and detailed comparisons as TCP and UDP have significant differences w.r.t to packet loss. 


**5) Are the parameters of the experiment meaningful? Are the ranges 
over which parameters vary meaningful and representative?**

The parameters of the experiment are meaningful. As this is a Routed network, having delay in the range of 100ms - 300ms is fair. The number of link failures considered is also fair as only single or double link failures happen in most networks.


**6) Have the authors sufficiently addressed the possibility of interactions 
between parameters?**

There is no mention about the interactions between the parameters.


**7) Are comparisons made reasonably? Is the baseline selected for comparison appropriate 
and realistic?**

Yes the comparisons are made reasonably as the comparison is between UDP and TCP which are both Transport Layer protocols.




## Communicating results


**1) Do the authors report the quantitative results of their experiment?**

Yes. They have provided both the Raw data obtained and the Quantitative results in the form of Bar Graphs.



**2) Is there information given about the variation and/or distribution of 
experimental results?**

No. there is no information about the variation and/or distribution of the experiment results. No statistics have been provided as well.


**3) Do the authors practice *data integrity* - telling the truth about their data, 
avoiding ratio games and other practices to artificially make their results seem better?**

Yes, they practice Data Integrity. There is no manipulation of the Data or the Results.


**4) Is the data presented in a clear and effective way? If the data is presented in 
graphical form, is the type of graph selected appropriate for the "story" that 
the data is telling?** 

Yes, the data is presented in a clear way but the experiment results lack statistical information like range, mean etc. 
The graph they have used does convey their results, but doesn’t include the confidence interval as mentioned earlier. 


**5) Are the conclusions drawn by the authors sufficiently supported by the 
experiment results?**

Yes, all the conclusions drawn by the author are sufficiently supported by their experiment results.

## Reproducible research



**1) Did the authors include instructions for reproducing the experiment in 3 ways (Raw data -> Results, 
Existing experiment setup -> Data, and Set up experiment)? Are the instructions clear
and easy to understand?**

Yes there are instructions for reproducing the experiment in three ways (Raw data -> Results, Existing experiment setup -> Data, and Set up experiment). Most of the instructions were clear and easy to understand but there were a few ambiguous ones, like : 

* There could have been clearer and easier instructions for the XORP installation procedure.
* They could have specified the format for saving the output files as this was an issue while using their R script to communicate the results obtained through our experiment. These names had to be taken from their R script. 


**2) Were you able to successfully produce experiment results?** 

Yes, it was feasible to produce the experiment results successfully. 


**3) How long did it take you to run this experiment, from start to finish?**

It took around 2 and a half hours to complete entire experiment from reserving the resources.  

**4) Did you need to make any changes or do any additional steps beyond the documentation in order to successfully complete this experiment? Describe *in detail*. How long did these extra steps or changes take to figure out?**

Yes, a few steps were required. 
The bash script `start-xorp.sh` could not be run with the given command which is **“av1540@router-1:/local/xorp_autostart$ /bin/bash start-xorp.sh”**
after moving to the folder **“xorp_autostart”**, `bash start-xorp.sh` did the job.

As mentioned earlier, there was a confusion while naming the output files which required referring their R script in order to coordinate the output file names. 

It took about 2 to 5 minutes to figure these out. 

**5) In the [lecture on reproducible experiments](http://witestlab.poly.edu/~ffund/el6383/files/Reproducible+experiments.pdf), we mentioned six degrees of reproducibility. How would you characterize this experiment - where does it fall on the six degrees of reproducibility?**

Since this experiment required considerable amount of effort, I would characterize this as one having a Degree 3 reproducibility. 


## Other comments to authors

1. A range of values might have been taken for the different experiment subsets. Also, a confidence interval would have been better instead of a single value for each experiment subset.
2. A more suitable plot style (barplots with error bars) would have been better to represent the data.
3. Installation of XORP was very time consuming and required a lot of effort. Could have automated this part.




