# Binary Search Trees (BST) in Ruby

This repo contains one possible implementation of a binary search tree in Ruby. I am posting it because a routine Google search revealed there are surprisingly few sources that have a good (legible and working) Ruby implementation of the core methods of a BST. So, for those who are taking a CS class on data structures or need a refresher to prepare for the whiteboarding part of a technical interview, this repo might be of interest to you.

There is no one right way to skin a cat, and neither is there one right way to write a BST class. My methods are all recursive, but iterative methods are possible too in some cases. And there are assuredly efficiency gains to be made within the recursive algorithms (e.g. some of the checks for `.nil?` could probably be refactored)--this is all fairly unpolished. But I think it's helpful to see others' approaches even if they might be suboptimal (I know I've benefited from the Internet's collective Ruby wisdom countless times), so I hope this provides some food for thought on one way to approach BSTs in Ruby.

Methods present:
```
#add_value
#has_value?
#delete_value  (with one small bug, see .rb file)

#size
#height
#height_balanced?
#valid_bst?
#identical_trees?
#subtree_of?

#breadth_first (breadth-first traversal)
#inorder   (depth-first traversal, builds a sorted array or an ascending linked list)
#preorder  (depth-first traversal)
#postorder (depth-first traversal)

#leaf?
#total_leaves

#to_bst  (converts a sorted array into a height-balanced BST)

(fragments of Node, Queue, and LinkedList classes included to assist in operations,
 which are of course better separated into individual files, which will happen if
 this repo expands)
```

What's missing? Well, a `#delete` method that works properly at a non-full root (I welcome any suggestions), and a `#rotation` method that would self-balance the tree when new items are added that cause the tree to become unbalanced. (There are many flavors of these: [click here](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree).)