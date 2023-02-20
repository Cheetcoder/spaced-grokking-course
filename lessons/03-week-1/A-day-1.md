# Day 1: Tree DFS, BFS

Study Patterns Tree Depth First Search and Tree Breadth First Search from https://www.designgurus.io/course-play/grokking-the-coding-interview



## Binary Tree Node

```golang
type TreeNode struct {
    val int
    left *TreeNode
    right *TreeNode
}

// Create Node with 1 element
root := &TreeNode{val: 3, left: nil, right: nil}
```

## Binary tree: DFS (recursive)

```golang
func dfs(root *TreeNode) int {
    if root == nil {
        return 0
    }

    ans := 0

    // do logic
    ans += dfs(root.left)
    ans += dfs(root.right)
    return ans
}

```

## Binary tree: DFS (iterative)

```golang
func dfs(root *TreeNode) int {
    if root == nil {
        return 0
    }

    stack := []*TreeNode{root}
    ans := 0

    for len(stack) > 0 {
        node := stack[len(stack)-1]
        stack = stack[:len(stack)-1]
        // do logic
        if node.left != nil {
            stack = append(stack, node.left)
        }
        if node.right != nil {
            stack = append(stack, node.right)
        }
    }

    return ans
}
```


## Binary tree: BFS


```golang
package main

import (
    "container/list"
)

func fn(root *TreeNode) int {
    queue := list.New()
    queue.PushBack(root)
    ans := 0

    for queue.Len() > 0 {
        current_length := queue.Len()
        // do logic for current level

        for i := 0; i < current_length; i++ {
            node := queue.Remove(queue.Front()).(*TreeNode)
            // do logic
            if node.left != nil {
                queue.PushBack(node.left)
            }
            if node.right != nil {
                queue.PushBack(node.right)
            }
        }
    }

    return ans
}
/**
Note that in the Go code, we used a linked list from the container package 
as a queue since Go does not have a built-in queue data structure. 
We also used the list.Len() method to get the length of the queue instead of the len() function.
**/
```

## Resources

- Estimated completion time: 4.5-9 hours 
- https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course-data-structures-and-algorithms/707/traversals-trees-graphs/
- Code Templates: https://leetcode.com/explore/interview/card/cheatsheets/720/resources/4723/ 
- https://github.com/TSiege/Tech-Interview-Cheat-Sheet#binary-tree 