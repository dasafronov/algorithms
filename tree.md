# Tree

+ [Binary Tree Inorder Traversal](#binary-tree-inorder-traversal)
+ [Symmetric Tree](#symmetric-tree)
+ [Maximum Depth Of Binary Tree](#maximum-depth-of-binary-tree)
+ [Same Tree](#same-tree)
+ [Invert Binary Tree](#invert-binary-tree)
+ [Path Sum](#path-sum)
+ [Binary Tree Level Order Traversal](#binary-tree-level-order-traversal)
+ [Subtree Of Another Tree](#subtree-of-another-tree)
+ [Kth Smallest Element In a BST](#kth-smallest-element-in-a-bst)
+ [Validate Binary Search Tree](#validate-binary-search-tree)
+ [Binary Search Tree Iterator](#binary-search-tree-iterator)

## Binary Tree Inorder Traversal

https://leetcode.com/problems/binary-tree-inorder-traversal/

```python
    
```

## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/

```python
    def isSymmetric(self, root: 'TreeNode') -> 'bool':

    def symmetric(p1, p2):
        if p1 and p2:
            return (p1.val == p2.val and symmetric(p1.left, p2.right) and
                    symmetric(p1.right, p2.left))
        else:
            return p1 is p2

    if not root:
        return True
    return symmetric(root.left, root.right)

```

## Maximum Depth Of Binary Tree

https://leetcode.com/problems/maximum-depth-of-binary-tree/

```python

```

## Same Tree

https://leetcode.com/problems/same-tree/

```python

```

## Invert Binary Tree

https://leetcode.com/problems/invert-binary-tree/

```python
def invertTree(self, root: TreeNode) -> TreeNode:
    if root is None:
        return root
    root.right, root.left = root.left, root.right
    self.invertTree(root.right)
    self.invertTree(root.left)
    return root

```

## Path Sum

https://leetcode.com/problems/path-sum/

```python

```

## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/

```python

```

## Subtree Of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/

```python

```

## Kth Smallest Element In a BST

https://leetcode.com/problems/kth-smallest-element-in-a-bst/

```python

```

## Validate Binary Search Tree

https://leetcode.com/problems/validate-binary-search-tree/

```python

```

## Binary Search Tree Iterator

https://leetcode.com/problems/binary-search-tree-iterator/

```python

```
