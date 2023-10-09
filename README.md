## GFG Problem Of The Day

### Today - 09 October 2023
### Que - Height of Binary Tree
The problem can be found at the following link: [Question Link](https://practice.geeksforgeeks.org/problems/height-of-binary-tree/1)

![](https://badgen.net/badge/Level/Easy/green)

### My Approach
To determine the height of a binary tree, I used a recursive approach. 
- Starting from the root node, I calculate the height of the left and right subtrees recursively and return the maximum of the two heights, plus one.

### Time and Auxiliary Space Complexity

- **Time Complexity**: The time complexity of this solution is `O(n)`, where `n` is the number of nodes in the binary tree. This is because I visit each node once, and the work done at each node is constant.

- **Auxiliary Space Complexity**: The auxiliary space complexity is `O(h)`, where `h` is the height of the binary tree. This space is used for the recursive call stack. In the worst case, for a skewed tree, the space complexity is `O(n)`, but for a balanced tree, it is `O(log n)`.

### Code (C++)
```cpp
class Solution {
public:
    int height(struct Node* node) {
        if (!node)
            return 0;

        return max(height(node->left), height(node->right)) + 1;
    }
};
```
### Contribution and Support

I always encourage contributors to participate in the discussion forum for this repository.

If you have a better solution or any queries / discussions related to the `Problem of the Day` solution, please visit our [discussion section](https://github.com/getlost01/gfg-potd/discussions). We welcome your input and aim to foster a collaborative learning environment.

If you find this solution helpful, consider supporting us by giving a `⭐ star` to the [getlost01/gfg-potd](https://github.com/getlost01/gfg-potd) repository.


![Total number of repository visitors](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)
