# P7-huffman

Cooperated on huffman encoding and decoding

Decoding reads the input in bits, create a tree with the input, then runs through the tree to write 8-bits
for all leaf node. (bit==0, go left; bit==1, go right; leaf node, read data)Read and write until 
reading PSEUDO_EOF, which is end of sequence.

Greedy algorithm and priority queues are used for compress. Find the frequency of the indices, add huffnodes 
with info of index,freq[index], and two null subnodes to queue; remove two smallest nodes in the queue, 
let them be the left and the right subnode of a node N, then add N back into the queue with its weight, or
freq, being the sum of its left and right subnode. Repeat until the tree is complete.
