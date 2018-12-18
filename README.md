# FoodVendorClustering
Estimating the density of NYC food vendors based on NYCDOH and NYPD violation data from the Environmental Control Board

Formulation:
Getting a violation issued does not neccessarily mean that the vendor was in the wrong, since the DOH and NYPD have quotas to meet.
If a vendor was so inclined to not want to deal with an inspector or keep his/her mobile food cart and vending practices up to code, then they can use this data to avoid certain locations at certain times of the day. This can also help struggling food permit owners who can't afford to pay exorbitant violation penalties.

Approach:
Using Kernel Density Estimation on a Time (violation issued) versus Block Number plot, our goal was to see which block numbers were issued the most violations over the course of 24 hours. We accomplished this by finding clusters that represnt the frequency of tickets being issued around that block number givin the time of day.

Evaluation and Interpretation:
We first tested a smaller sample of data (1000 samples) that produced clustering coordinates and then used the full data set (9000 samples) that also produced clustering coordinates.
The results from the clusters are interpeted as (from the first cluster coordinate) vending on block numbers around block 842 at 1pm, would indicate that that someone with authority (DOH inspector or NYPD) to issue a violation is likely to be around there. 

Some shortcomings of approach were using a density estimation algorithim on a data set that ended up not being circular, which Kernel Density Estimation is more suitable for. 

The jupyter notebook is divided into 5 sections with the python code commented on


