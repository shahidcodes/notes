# Problems

#### 1. Given a list of numbers and a number `k`, return whether any two numbers from the list add up to `k`. 
*asked by Google*


Solution: 
	1. [JSBIN](https://jsbin.com/nemeboxini/edit?js,console)  
	2. [jsben.ch](http://jsben.ch/hiASj)

#### 2. Given an array of integers, return a new array such that each element at index `i` of the new array is the product of all the numbers in the original array except the one at `i`.
For example, if our input was `[1, 2, 3, 4, 5]`, the expected output would be `[120, 60, 40, 30, 24]`. If our input was `[3, 2, 1]`, the expected output would be `[2, 3, 6]`.

**Solution:**
1. [jsbin](https://jsbin.com/kidixuf/edit?js,console)
2. [jsben.ch](http://jsben.ch/rujQZ)
3. [gist.github.com](https://gist.github.com/d89f6f91f34f3f752e7f13dd99ce81e5)

#### 3. Given the root to a binary tree, implement  `serialize(root)`, which serializes the tree into a string, and  `deserialize(s)`, which deserializes the string back into the tree.

For example, given the following  `Node`  class
```python
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

```
The following test should pass:
```python
node = Node('root', Node('left', Node('left.left')), Node('right'))
assert deserialize(serialize(node)).left.left.val == 'left.left'
```
**Solution:**
We can solve it two ways: 
1. Using build-in data structure and modules such as json, and dict
[https://repl.it/@ShahidKamal/tree-serializedeserialize-problem-asked-by-google](https://repl.it/@ShahidKamal/tree-serializedeserialize-problem-asked-by-google)
2. Using built-in data structure and custom encoder and decoder. For example we can use dict to and write custom encoder to encode to string and decoder to convert back to `Node` object
3. Using custom encoder/decoder for `Node` object. This is very difficult and requires one to have understanding  of lexer.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzMzc1NzAyNjMsLTE3ODA4OTM4MDEsLT
E0OTg2ODcwNDMsLTk3NTE5NzczNl19
-->