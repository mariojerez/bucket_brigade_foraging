# Foraging using Bucket Brigade and Defense Against Parasites
I developed these programs in undergrad to simulate two foraging behaviors found among Leafcutter (Atta) ant colonies that I found interesting. I simulated the behaviors using NetLogo, and built off of the NetLogo Ants model.

## Running the Simulations
The simplest way to run the simulations is through NetLogo Web.
1. Visit https://netlogoweb.org/ and click on NetLogo Web
2. Select *Choose File*
3. Upload the NetLogo file from this repository that you wish to try
4. Adjust the hyperparameters of the model using the sliders or by entering a quantity
5. Click *setup*
6. Click *go*
7. If you wish to start over with different parameter values, click *go* to pause, and repeat steps 4 through 6.

## Bucket Brigade
Some Atta foragers use a task partitioning strategy called Bucket Brigade when transporting leaf fragments from a harvest site that is far away from the nest (Hubbell 1980). In this system, a leaf fragment is cut by a large worker which is then further partitioned by other workers when it lands on the ground. Workers which specialize in transporting leaves then pick up these fragments and scurry down the trail towards the nest until they come across another ant with its jaws free. The former ant directly transfers the leaf to the latter and either returns to the harvest site or becomes the recipient of another ant, while the latter ant either carries the leaf back to the nest or passes the leaf off to another worker that it encounters. An alternative method uses indirect transfer, where ants carry leaf fragments a certain distance along the trail before dropping them and returning to collect more. These dropped leaves then get picked up and transported by other ants further down the chain. This process gets repeated until one of the leaf carriers reaches the nest. This kind of task partitioning during harvest is theorized to make the transport faster and more efficient by reinforcing the trail with more pheromones, increasing the amount of contact between ants and the food and therefore increasing exchange of information regarding the quality of food which impacts the intensity of worker recruitment (Hölldobler et al. 73-4).

I implemented the indirect transfer method described above in **bucket brigade.nlogo**.

## Defense Against Parasites
Some Leafcutter ant colonies are threatened by phorid flies, which lay eggs in the necks of ants while they are carrying leaf fragments to their nest. To defend against this, colonies exhibit hitchhiking behavior in which minims–the smallest sub-cast in the colony–ride on the leaf fragments being carried to the nest to defend the larger ant from phorid flies. Hitchhiking seems to serve three uses: defense against parasites, providing minims nutrition as they lick sap from the leaf fragments, and cleaning the leaf before it enters the nest (Linksvayer 98).

In **Ants + phorid flies.nlogo**, minims, the white, smaller ants, follow the pheromones that are released by ants carrying leaves to the nest. When a minim makes contact with one of these ants, the transporting ant turns green, meaning that it is protected from parasites. For every time step that an ant carries resources without a hitchhiker, it has a probability of dying, causing the foraging population to decrease. Increasing the *parasite-intensity* increases this probability, while the *starting-foraging-population* and *hitchiking-population* parameters set the number of foraging ants at timestep 0 and the number of minims respectively.

## References
Hölldobler Bert, and Edward O Wilson. The Leafcutter Ants : Civilization by Instinct. 1st ed., Norton, 2011.

Hubbell, Stephen P, et al. “Foraging by Bucket-Brigade in Leaf-Cutter Ants.” Biotropica, vol. 12, no. 3, 1980, pp. 210–210., doi:10.2307/2387973.

Linksvayer, Timothy A., et al. “The Function of Hitchhiking Behavior in the Leaf-Cutting Ant Atta Cephalotes.” Biotropica, vol. 34, no. 1, 2002, pp. 93–100., doi:10.1646/0006-3606(2002)034[0093:tfohbi]2.0.co;2.

Wilensky, U. (1997). NetLogo Ants model. http://ccl.northwestern.edu/netlogo/models/Ants. Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

Wilensky, U. (1999). NetLogo. http://ccl.northwestern.edu/netlogo/. Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.
