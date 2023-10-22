- A `tree` represents a *hierarchical nature* of a structure in a *graphical form*
	- *elements* or `nodes`, which each node linked to its successors.
- `Root`, *top* of the `tree`.
- `Branches`, `edges`, `lines`, `paths`; *links from a node to its successors of a node*.
- The successors of a `node` is called its `child nodes`.
- The predecessor of a `node` is called its `parent`.
- A `tree` is considered a `binary tree` if all its nodes have *two* `(2)` child `nodes` at most.
	- Each `node` in a `tree` has exactly *one* `(1)` parent except for the `root node`, which has no parent.
	- `Siblings`, *nodes* that have the same `parent`.
	- `External node` or `leaf node`, a *node* that has no *child nodes*.
	- `Internal node`, a *node* that have *child nodes*.
- `Subtree`, a `tree` within a `tree`.
- **Level**, a `node` is a measure of its distance from the `root`.
- **Depth**, the highest level of the `tree`.
- **Degree**, the *number of child nodes* in a `subtree`.

###### Tree Traversal
- **Traversal** - is the process of *visiting all the nodes* in a specific order.
	- `Breadth-First` or `Level Order` - *Nodes are visited by level*: `1`, `2`, `3`, `4`, `5`.
	- `Depth-First`
		- **Inorder** (`Left`, `Root`, `Right`): `4`, `2`, `5`, `1`, `3`
		*Start with the bottommost left subtree. Once the root in Level* `0` *is visited, proceed to the bottommost right subtree.* 
		- **Preorder** (`Root`, `Left`, `Right`): `1`, `2`, `4`, `5`, `3`
		*Start with the root in Level* `0` *then continue with the left subtree.*

		- **Postorder** (`Left`, `Right`, `Root`): `4`, `5`, `2`, `3`, `1`
		*Start with the bottommost left subtree then proceed to the other subtrees. The root in Level* `0` *is the last node visited.*

###### Programming Trees
- **JTree** is a *Java Swing component* that displays a set of *hierarchical data* as an outline. It is included in the `javax.swing` package.
- `DefaultMutableTreeNode`, is used to represent a *general-purpose* node in a tree data structure. It is included in the `javax.swing.tree` package.
- `add()` method removes a *node* from its `parent` and makes it a `child` of another *node* by adding it to the end of that node's `child` array. Other java methods are:
	- `getRoot()`: *Returns* the root of the tree that contains the *node*
	- `children()`: *Creates* and *returns* a `forward-order` *enumeration* of a node's children
	- `getChildCount()`: *Return* the number of children that a *node* has
	- `getParent()`: *Returns* a node's `parent` or `null` if it has no `parent`
	- `isNodeSibling()`: *Returns* `true` if a *node* is a sibling of the other *node*
	- `getPreviousSibling()`: *Returns* the previous `sibling` of a *node* in the `parent's children` array
	- `getNextSibling()`: *Returns* the next `sibling` of a *node* in the `parent's children` array
	- `getSiblingCount()`: *Returns* the `number` of `siblings` of a *node*
	- `isLeaf()`: *Returns* `true` if a *node* has no `children`
	- `getLeafCount()`: *Returns* the total number of *leaves* that are *descendants* of a *node*
	- `getLevel()`: *Returns* the number of `levels` above a *node*
	- `getDepth()`: *Return* the highest `level` above a *node*
	- `getChildCount()`: *Returns* the number of `children` (degree) of a *node*
	- `breadthFirstEnumeration()`: *Creates* and *returns* an `enumeration` that traverses the subtree rooted at a *node* in `breadth-first order`
	- `preorderEnumeration()`: *Creates* and *returns* an `enumeration` that traverses the subtree rooted at a *node* in `preorder`
	- `postorderEnumeration()`: *Creates* and *returns* an `enumeration` that traverses the subtree rooted at this a in `postorder`