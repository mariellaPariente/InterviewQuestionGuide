# Convert Binary Tree to its Mirror
Description: 
Given a binary tree, write an algorithm to invert the tree.

## The Problem: 
You may ask yourself when and how would inverting a binary tree be useful. As a newbie I asked myself that same question. The answer is, it is useful in showing how you breakdown a problem and how well you understand data structures. If you are like me and like to see practical examples to help you learn, well you are out of luck. A quick Google search "practical applications of mirroring binary trees” just returned the controversy of this question being asked in interviews. Take a look at the links below for a fun read of the perception of this particular problem.

[Hackerrank's take on Tree questions](https://blog.hackerrank.com/the-unhealthy-obsession-with-tree-questions/)

[Famous Tweet](https://twitter.com/mxcl/status/608682016205344768)

[Why is it good to know?](https://thecodebarbarian.com/i-dont-want-to-hire-you-if-you-cant-reverse-a-binary-tree)

### The good news: 
The process of Mirroring a binary tree is very straightforward to understand.

## Problem Description: Mirror a binary Tree
Mirroring is type of tree-manipulation problem, which also includes inverting parent-child relationships. In this example the mirror of an input tree is another binary tree with left and right children swapped resulting in a "mirror" image of the input tree.   

## Example:
Starting Tree T - Input tree

![Image Inverted BT](https://raw.githubusercontent.com/mariellaPariente/InterviewQuestionGuide/master/Trees/treeImages/inverted%20BT.png)

Resulting Tree after mirroring M(T) - Output Tree

![Image Input BT](https://raw.githubusercontent.com/mariellaPariente/InterviewQuestionGuide/master/Trees/treeImages/Input%20tree%20BT.png)


## The Solution:
    Perform an inorder traversal and swap the children and recursively solve the smaller sub-problems of the left and the right sub-tree
    
    There are three steps that are executed for every node of the BT
    1. If the tree is empty return NULL
    2. Call the mirror function for the left-subtree or the right-subtree
    3. For every node swap its left and right child 

## Pseudocode:
     void mirror (struct node* node) {
	// base case: if tree is empty
	if (node == NULL)
		return;
	
	else
	{
		struct node* temp;

		mirror(node->left);
		mirror(node->right);

 		// swap left subtree with right subtree
		temp = node->left;
		node->left = node->right;
		node->right = temp;
	}

}
## Walking Through the Tree visually:
	Node D Nulls
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/NullD.png) 

	Node E Nulls
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/NullsE.png) 

	Swap D and E (First Swap)
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/SwapDandE.png) 

	Swap F and G 
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/SwapFandG.png) 

	Swap B and C
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/SwapBandC.png) 
   
## Walking Through the pseudo code until the first Swap:
![Image Input BT](https://github.com/mariellaPariente/InterviewQuestionGuide/blob/master/Trees/treeImages/firstSwap.png)

## Related Topics
[Inorder, Preorder and Postorder traversals](https://www.geeksforgeeks.org/dfs-traversal-of-a-tree-using-recursion/)
	
