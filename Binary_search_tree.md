##### Binary Search Tree

## Overview

This is a tree where left side of the root always have lower values and right side always have higher values.

![alt text](https://upload.wikimedia.org/wikipedia/commons/d/da/Binary_search_tree.svg "Logo Title Text 1")

Sample node declaration (C++):

```
struct node {
    int value;
    node *left;
    node *right;
};
```

Sample Search:

```
node *btree::search(int key, node *leaf)
{
  if(leaf!=NULL)
  {
    if(key==leaf->key_value)
      return leaf;
    if(key<leaf->key_value)
      return search(key, leaf->left);
    else
      return search(key, leaf->right);
  }
  else return NULL;
}
```
