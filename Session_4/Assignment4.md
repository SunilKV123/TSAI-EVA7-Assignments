# EVA7 - Assignment 4 #
1. Write a neural network that can:
	Take 2 inputs:
	1. An image from the MNIST dataset (say 5), and
	2. A random number between 0 and 9, (say 7)
	and Gives two outputs:
	1. the "number" that was represented by the MNIST image (predict 5), and
	2. the "sum" of this number with the random number and the input image to the network (predict 5 + 7 = 12)
	<p align ="center">
	  <img  src="resource/assign4.png">			  
	</p>
	3. Can mix fully connected layers and convolution layers
	4. Can use one-hot encoding to represent the random number input as well as the "summed" output.
		a. Random number (7) can be represented as 0 0 0 0 0 0 0 1 0 0
		b. Sum (13) can be represented as:
			b1. 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0
			b2. 0b1101 (remember that 4 digits in binary can at max represent 15, so we may need to go for 5 digits. i.e. 10010
2. Your code MUST be:
	1. well documented (via readme file on GitHub and comments in the code)
	2. must mention the data representation
	3. must mention your data generation strategy (basically the class/method you are using for random number generation)
	4. must mention how you have combined the two inputs (basically which layer you are combining)
	5. must mention how you are evaluating your results 
	6. must mention "what" results you finally got and how did you evaluate your results
	7. must mention what loss function you picked and why!
	8. training MUST happen on the GPU
	9. Accuracy is not really important for the SUM
3. Once done, upload the code with short training logs in the readme file from colab to GitHub, and share the GitHub link (public repository)

### Training logs ###
Training Epoch: 1 [0/59]	Loss: 5.2718	LR: 0.010000
Training Epoch: 1 [10/59]	Loss: 5.0588	LR: 0.010000
Training Epoch: 1 [20/59]	Loss: 4.6491	LR: 0.010000
Training Epoch: 1 [30/59]	Loss: 4.1022	LR: 0.010000
Training Epoch: 1 [40/59]	Loss: 3.7026	LR: 0.010000
Training Epoch: 1 [50/59]	Loss: 3.4171	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 1, Average loss: 0.0033, Digit Accuracy: 0.9129, Sum Accuracy: 0.0981

Training Epoch: 2 [0/59]	Loss: 3.2545	LR: 0.010000
Training Epoch: 2 [10/59]	Loss: 3.1639	LR: 0.010000
Training Epoch: 2 [20/59]	Loss: 3.1006	LR: 0.010000
Training Epoch: 2 [30/59]	Loss: 3.0736	LR: 0.010000
Training Epoch: 2 [40/59]	Loss: 3.0388	LR: 0.010000
Training Epoch: 2 [50/59]	Loss: 3.0358	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 2, Average loss: 0.0030, Digit Accuracy: 0.9501, Sum Accuracy: 0.0985

Training Epoch: 3 [0/59]	Loss: 2.9929	LR: 0.010000
Training Epoch: 3 [10/59]	Loss: 2.9617	LR: 0.010000
Training Epoch: 3 [20/59]	Loss: 2.9392	LR: 0.010000
Training Epoch: 3 [30/59]	Loss: 2.9451	LR: 0.010000
Training Epoch: 3 [40/59]	Loss: 2.9159	LR: 0.010000
Training Epoch: 3 [50/59]	Loss: 2.9350	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 3, Average loss: 0.0029, Digit Accuracy: 0.9757, Sum Accuracy: 0.1033

Training Epoch: 4 [0/59]	Loss: 2.9123	LR: 0.010000
Training Epoch: 4 [10/59]	Loss: 2.8741	LR: 0.010000
Training Epoch: 4 [20/59]	Loss: 2.8998	LR: 0.010000
Training Epoch: 4 [30/59]	Loss: 2.8998	LR: 0.010000
Training Epoch: 4 [40/59]	Loss: 2.8488	LR: 0.010000
Training Epoch: 4 [50/59]	Loss: 2.8313	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 4, Average loss: 0.0028, Digit Accuracy: 0.9782, Sum Accuracy: 0.0999

Training Epoch: 5 [0/59]	Loss: 2.8716	LR: 0.010000
Training Epoch: 5 [10/59]	Loss: 2.8457	LR: 0.010000
Training Epoch: 5 [20/59]	Loss: 2.8673	LR: 0.010000
Training Epoch: 5 [30/59]	Loss: 2.8415	LR: 0.010000
Training Epoch: 5 [40/59]	Loss: 2.8385	LR: 0.010000
Training Epoch: 5 [50/59]	Loss: 2.8405	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 5, Average loss: 0.0028, Digit Accuracy: 0.9815, Sum Accuracy: 0.0991

Training Epoch: 6 [0/59]	Loss: 2.8075	LR: 0.010000
Training Epoch: 6 [10/59]	Loss: 2.7998	LR: 0.010000
Training Epoch: 6 [20/59]	Loss: 2.8023	LR: 0.010000
Training Epoch: 6 [30/59]	Loss: 2.8118	LR: 0.010000
Training Epoch: 6 [40/59]	Loss: 2.8115	LR: 0.010000
Training Epoch: 6 [50/59]	Loss: 2.7761	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 6, Average loss: 0.0027, Digit Accuracy: 0.9845, Sum Accuracy: 0.0990

Training Epoch: 7 [0/59]	Loss: 2.7446	LR: 0.010000
Training Epoch: 7 [10/59]	Loss: 2.7354	LR: 0.010000
Training Epoch: 7 [20/59]	Loss: 2.7439	LR: 0.010000
Training Epoch: 7 [30/59]	Loss: 2.7250	LR: 0.010000
Training Epoch: 7 [40/59]	Loss: 2.6828	LR: 0.010000
Training Epoch: 7 [50/59]	Loss: 2.7061	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 7, Average loss: 0.0026, Digit Accuracy: 0.9859, Sum Accuracy: 0.1437

Training Epoch: 8 [0/59]	Loss: 2.6718	LR: 0.010000
Training Epoch: 8 [10/59]	Loss: 2.6158	LR: 0.010000
Training Epoch: 8 [20/59]	Loss: 2.5985	LR: 0.010000
Training Epoch: 8 [30/59]	Loss: 2.5859	LR: 0.010000
Training Epoch: 8 [40/59]	Loss: 2.5720	LR: 0.010000
Training Epoch: 8 [50/59]	Loss: 2.5261	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 8, Average loss: 0.0025, Digit Accuracy: 0.9885, Sum Accuracy: 0.2216

Training Epoch: 9 [0/59]	Loss: 2.5084	LR: 0.010000
Training Epoch: 9 [10/59]	Loss: 2.4333	LR: 0.010000
Training Epoch: 9 [20/59]	Loss: 2.3897	LR: 0.010000
Training Epoch: 9 [30/59]	Loss: 2.3802	LR: 0.010000
Training Epoch: 9 [40/59]	Loss: 2.3239	LR: 0.010000
Training Epoch: 9 [50/59]	Loss: 2.2761	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 9, Average loss: 0.0022, Digit Accuracy: 0.9854, Sum Accuracy: 0.3605

Training Epoch: 10 [0/59]	Loss: 2.2303	LR: 0.010000
Training Epoch: 10 [10/59]	Loss: 2.1972	LR: 0.010000
Training Epoch: 10 [20/59]	Loss: 2.1696	LR: 0.010000
Training Epoch: 10 [30/59]	Loss: 2.0980	LR: 0.010000
Training Epoch: 10 [40/59]	Loss: 2.1071	LR: 0.010000
Training Epoch: 10 [50/59]	Loss: 2.0483	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 10, Average loss: 0.0020, Digit Accuracy: 0.9902, Sum Accuracy: 0.4110

Training Epoch: 11 [0/59]	Loss: 2.0070	LR: 0.010000
Training Epoch: 11 [10/59]	Loss: 1.9880	LR: 0.010000
Training Epoch: 11 [20/59]	Loss: 1.9384	LR: 0.010000
Training Epoch: 11 [30/59]	Loss: 1.8808	LR: 0.010000
Training Epoch: 11 [40/59]	Loss: 1.9044	LR: 0.010000
Training Epoch: 11 [50/59]	Loss: 1.8214	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 11, Average loss: 0.0018, Digit Accuracy: 0.9900, Sum Accuracy: 0.5553

Training Epoch: 12 [0/59]	Loss: 1.8179	LR: 0.010000
Training Epoch: 12 [10/59]	Loss: 1.7585	LR: 0.010000
Training Epoch: 12 [20/59]	Loss: 1.7466	LR: 0.010000
Training Epoch: 12 [30/59]	Loss: 1.7025	LR: 0.010000
Training Epoch: 12 [40/59]	Loss: 1.6444	LR: 0.010000
Training Epoch: 12 [50/59]	Loss: 1.6498	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 12, Average loss: 0.0016, Digit Accuracy: 0.9907, Sum Accuracy: 0.5490

Training Epoch: 13 [0/59]	Loss: 1.6066	LR: 0.010000
Training Epoch: 13 [10/59]	Loss: 1.5918	LR: 0.010000
Training Epoch: 13 [20/59]	Loss: 1.5769	LR: 0.010000
Training Epoch: 13 [30/59]	Loss: 1.5404	LR: 0.010000
Training Epoch: 13 [40/59]	Loss: 1.5444	LR: 0.010000
Training Epoch: 13 [50/59]	Loss: 1.5000	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 13, Average loss: 0.0014, Digit Accuracy: 0.9898, Sum Accuracy: 0.6692

Training Epoch: 14 [0/59]	Loss: 1.4599	LR: 0.010000
Training Epoch: 14 [10/59]	Loss: 1.4546	LR: 0.010000
Training Epoch: 14 [20/59]	Loss: 1.4094	LR: 0.010000
Training Epoch: 14 [30/59]	Loss: 1.3780	LR: 0.010000
Training Epoch: 14 [40/59]	Loss: 1.4038	LR: 0.010000
Training Epoch: 14 [50/59]	Loss: 1.3300	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 14, Average loss: 0.0013, Digit Accuracy: 0.9901, Sum Accuracy: 0.7566

Training Epoch: 15 [0/59]	Loss: 1.3446	LR: 0.010000
Training Epoch: 15 [10/59]	Loss: 1.2909	LR: 0.010000
Training Epoch: 15 [20/59]	Loss: 1.3028	LR: 0.010000
Training Epoch: 15 [30/59]	Loss: 1.2549	LR: 0.010000
Training Epoch: 15 [40/59]	Loss: 1.2276	LR: 0.010000
Training Epoch: 15 [50/59]	Loss: 1.2246	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 15, Average loss: 0.0012, Digit Accuracy: 0.9908, Sum Accuracy: 0.8420

Training Epoch: 16 [0/59]	Loss: 1.1972	LR: 0.010000
Training Epoch: 16 [10/59]	Loss: 1.2107	LR: 0.010000
Training Epoch: 16 [20/59]	Loss: 1.1799	LR: 0.010000
Training Epoch: 16 [30/59]	Loss: 1.1183	LR: 0.010000
Training Epoch: 16 [40/59]	Loss: 1.1215	LR: 0.010000
Training Epoch: 16 [50/59]	Loss: 1.1134	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 16, Average loss: 0.0011, Digit Accuracy: 0.9919, Sum Accuracy: 0.9192

Training Epoch: 17 [0/59]	Loss: 1.1059	LR: 0.010000
Training Epoch: 17 [10/59]	Loss: 1.0496	LR: 0.010000
Training Epoch: 17 [20/59]	Loss: 1.0558	LR: 0.010000
Training Epoch: 17 [30/59]	Loss: 1.0330	LR: 0.010000
Training Epoch: 17 [40/59]	Loss: 1.0399	LR: 0.010000
Training Epoch: 17 [50/59]	Loss: 1.0066	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 17, Average loss: 0.0010, Digit Accuracy: 0.9909, Sum Accuracy: 0.9596

Training Epoch: 18 [0/59]	Loss: 0.9712	LR: 0.010000
Training Epoch: 18 [10/59]	Loss: 1.0433	LR: 0.010000
Training Epoch: 18 [20/59]	Loss: 0.9864	LR: 0.010000
Training Epoch: 18 [30/59]	Loss: 0.9565	LR: 0.010000
Training Epoch: 18 [40/59]	Loss: 0.9560	LR: 0.010000
Training Epoch: 18 [50/59]	Loss: 0.9275	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 18, Average loss: 0.0009, Digit Accuracy: 0.9908, Sum Accuracy: 0.9563

Training Epoch: 19 [0/59]	Loss: 0.9788	LR: 0.010000
Training Epoch: 19 [10/59]	Loss: 0.8501	LR: 0.010000
Training Epoch: 19 [20/59]	Loss: 0.8521	LR: 0.010000
Training Epoch: 19 [30/59]	Loss: 0.8473	LR: 0.010000
Training Epoch: 19 [40/59]	Loss: 0.8943	LR: 0.010000
Training Epoch: 19 [50/59]	Loss: 0.8304	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 19, Average loss: 0.0008, Digit Accuracy: 0.9924, Sum Accuracy: 0.9604

Training Epoch: 20 [0/59]	Loss: 0.8368	LR: 0.010000
Training Epoch: 20 [10/59]	Loss: 0.8270	LR: 0.010000
Training Epoch: 20 [20/59]	Loss: 0.8662	LR: 0.010000
Training Epoch: 20 [30/59]	Loss: 0.8038	LR: 0.010000
Training Epoch: 20 [40/59]	Loss: 0.8204	LR: 0.010000
Training Epoch: 20 [50/59]	Loss: 0.7875	LR: 0.010000
<br/>Evaluating Network.....
<br/>Test set: Epoch: 20, Average loss: 0.0007, Digit Accuracy: 0.9918, Sum Accuracy: 0.9624


