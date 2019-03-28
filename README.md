# Simulated-annealing-lifting-QC-LDPC
Source code for article
Vasiliy Usatyuk und Ilya Vorobyev 
Simulated Annealing Method for Construction of High-Girth QC-LDPC Codes
 41st International Conference on Telecommunications and Signal Processing (TSP) 2018, 4-6 Jule, Athens, Greece
 It construct regular and irregular QC-LDPC codes with  multiple edge circulants from protograph with required minimal EMD value.

Simulated annealing lifting for high girth QC-LDPC include EMD optimization of protograph, which allow to decrease error-floor (by eliminate harmful Trapping Sets), or improve waterfall properties (by lifting of protograph with better threshold).
To use application call binary file with command:
binary -file Your_protograph_file -circulant size_of_circulant -upGirth check_condition_up_to_cycles -emd EMD_values -seed initial_value_for_random_generator -numberOfMatrices number_of_requirement_matrix -girth girth_size

Your_protograph_file
Contain number of columns(Variable nodes), rows (Check nodes)
1,0 value for circulant permutation block matrix, obtain by some optimization of LDPC codes ensemble (Density Evolution, Covariance Evolution, PEXIT chart and etc).
For Example:
simulatedAnnealingEMD.exe -file proto.txt -circulant 500 -upGirth 8 -emd 20 -seed 123 -numberOfMatrices 1 -girth 8
Proto.txt contain base matrix:
3 2
1 0 1
1 1 0

For construction multiple edge use 2,3 instead 1. Example:
simulatedAnnealingEMD.exe -file proto.txt -circulant 500 -upGirth 6 -emd 2 -seed 123 -numberOfMatrices 1 -girth 8
16 6
1 0 0 0 0 1 0 1 0 1 1 0 1 0 0 2
1 1 0 0 0 0 0 1 1 0 0 1 0 1 1 2
0 1 1 0 0 0 0 1 0 1 0 1 0 1 0 1
0 0 1 1 0 0 1 0 1 0 1 0 0 1 1 1

output:
16	6	500
440	-1	-1	-1	-1	0	-1	258	-1	203	0	-1	237	-1	-1	329&215	
53	75	-1	-1	-1	-1	-1	95	0	-1	-1	443	-1	0	238	284&257	
-1	104	363	-1	-1	-1	-1	67	-1	466	-1	5	-1	174	-1	425	
-1	-1	265	249	-1	-1	363	-1	59	-1	392	-1	-1	324	119	488	
-1	-1	-1	260	64	-1	429	-1	-1	383	402	-1	421	-1	348	97&222	
-1	-1	-1	-1	429	480	86	-1	234	-1	-1	114	41	-1	-1	392&402	







