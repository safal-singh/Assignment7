# Assignment7a 
**Maximum Receptive field calculation for GoogleNet**

r_out = r_in +  (k - 1) * j_in <br/>
j_out = j_in * s <br/>

where, <br/>
r_in - receptive field of the previous layer <br/>
r_out - receptive field of the current layer <br/>
j_in - jump of the previous layer <br/>
j_out - jump of the current layer <br/>
s - stride of current layer <br/>
k - kernel size of the current layer <br/>


| r_in |	j_in |	k	| s |	layer |
|------|--------|---|---|-------|
| 1 |	1 |	0 |	0 |	input |
| 7 |	2 |	7 |	2 |	conv |
| 11 | 	4 |	3 |	2 |	max pool | 
| 11	| 4	| 1 |	1 |	conv |
| 19	| 4	| 3	| 1	| conv |
| 27 |	8 |	3 |	2 |	max pool |
| 59	| 8	| 5	| 1	| concat1 |
| 91	| 8	| 5	| 1	| concat2 |
| 107	| 16	| 3	| 2	| max pool |
| 171	| 16	| 5	| 1	| concat3 |
| 235	| 16	| 5	| 1	| concat4 |
| 299	| 16	| 5	| 1	| concat5 |
| 363	| 16	| 5	| 1	| concat6 |
| 427	| 16	| 5	| 1	| concat7 |
| 459	| 32	| 3	| 2	| max pool |
| 587	| 32	| 5	| 1	| concat8 |
| 715	| 32	| 5	| 1	| concat9 |
| 907	| 32	| 7	| 1	| avg pool |

**For grouped convolutions, the network with maximum receptive field is considered.**
