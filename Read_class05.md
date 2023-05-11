# Linked Lists
## when we have a list then I want to make a change like delete an item I need to make many processes like delete item then make a shift in other and so on for each change; delete or add and I take many time.
* To solve this problem: In python we look to the item in lists separately as single units. And in each single unit I have a linked information with other so when I want to delete item, I just change a relation.
## What is linked list: it is a group of nodes; each node includes a data and next (which is like a pointer start from this node to next one)
## Now we don't have an index to know what the first item is so we use (Head) to know what the first item is then by using next we can continue moving to other items But When we moving, I don't mean the head when change its position (because if head do that it will change the start item that is mean I delete other one) to solve this problem we use
## (Current node) that will start from head then move to the next item to reach all.
## when I have a node with one pointer, we call it (Single linked list)
## And when I have a node with two pointer, we call it (Doubly linked list).