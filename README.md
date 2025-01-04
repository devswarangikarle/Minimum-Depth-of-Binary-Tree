# Minimum-Depth-of-Binary-Tree

Given a binary tree, find its minimum depth.
The minimum depth is the number of nodes along the shortest path from the root node down to the nearest leaf node.
Note: A leaf is a node with no children.

Constraints:

The number of nodes in the tree is in the range [0, 10^5].
-1000 <= Node.val <= 1000

class Solution: 
    def minDepth(self, root: TreeNode) -> int:

        if not root: return 0
        level, queue = 0, deque([root]) 

        while queue:

            level+= 1

            for x in range(len(queue)):

                n = queue.popleft()
                if not n.left and not n.right: return level

                if n.left : queue.append(n. left)
                if n.right: queue.append(n.right)
