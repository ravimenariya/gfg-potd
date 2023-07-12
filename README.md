## GFG Problem Of The Day

### 🎉 Announcement
I have created a Git Book that contains all previous editorials for my GFG-POTD solutions. You can visit **[here](https://gl01.gitbook.io/gfg-editorials/)** to access it and refer to my previous solutions. In the future, I intend to establish a contribution flow, where others can contribute their solutions to this Git Book. I would appreciate hearing your thoughts and views on this in the [discussion section](https://github.com/getlost01/gfg-potd/discussions).

----
### Today - 12 July 2023
### Que - Power Of Numbers

The problem can be found at the following link: [Question Link](https://practice.geeksforgeeks.org/problems/power-of-numbers-1587115620/1)

### My Approach

I have use the **modular exponentiation** algorithm to efficiently calculate the power with a logarithmic time complexity.

Here's the step-by-step explanation of the algorithm:

- Initialize a variable `res` to 1, which will store the final result.
- Enter a loop while `n` is not zero:
   - Check if the least significant bit of `n` is 1 by using the bitwise AND operator `n & 1`.
   - If the bit is 1, multiply `res` with `a` modulo `mod` and decrement `n` by 1.
   - If the bit is 0, square `a` modulo `mod` and divide `n` by 2.
- Finally, return the calculated result `res`.

For a more comprehensive understanding of binary exponentiation and modular exponentiation, I recommend reading this [article](https://www.geeksforgeeks.org/modular-exponentiation-power-in-modular-arithmetic/).

### Time and Auxiliary Space Complexity

- **Time Complexity**: The `powerexpo` function operates in `O(log N)` time complexity since we divide `n` by 2 at each step until it becomes zero. 

- **Auxiliary Space Complexity**: `O(1)` since we uses a constant amount of auxiliary space, independent of the input size,

### Code (C++)

```cpp
class Solution {
public:
    long long powerexpo(long long a, long long n) {
        int res = 1;
        while (n) {
            if (n & 1) {
                res = (res % mod * a % mod) % mod;
                --n;
            } else {
                a = (a % mod * a % mod) % mod;
                n >>= 1;
            }
        }
        return res;
    }

    long long power(int N, int R) {
        return powerexpo(N, R);
    }
};
```

### Contribution and Support

I always encourage contributors to participate in the discussion forum for this repository.

If you have a better solution or any queries / discussions related to the `Problem of the Day` solution, please visit our [discussion section](https://github.com/getlost01/gfg-potd/discussions). We welcome your input and aim to foster a collaborative learning environment.

If you find this solution helpful, consider supporting us by giving a `⭐ star` to the [getlost01/gfg-potd](https://github.com/getlost01/gfg-potd) repository.


![Total number of repository visitors](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)
