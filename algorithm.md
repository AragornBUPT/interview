# 重点题目

1. 花钱题：用1元，5元，11元凑出w元，要求使用张数最少（动态规划）
2. 二叉树递归前序遍历、中序遍历、后续遍历
3. 二叉树非递归遍历

<details>

```text
所有遍历的边界点（终止循环的条件）：cursor为nil（到头了，没有子节点了）并且栈为空（都遍历过了）
```

</details>

- 前序遍历

<details>

```text
把左边界依次压入栈，同时打印。
弹出的时候，不打印，将右节点压入栈
1）cursor=root
2）打印cursor，并将其压入栈，cursor=cursor.left，直到cursor为空
3）弹出栈顶节点，cursor=cursor.right
4）重复2、3，直到栈和cursor均为空
```

</details>

- 中序遍历

<details>

```text
把左边界依次压入栈。到头后，依次弹出并打印，获取其右节点，继续遍历其左边界
1、cursor=root
2、将cursor压入栈，cursor=cursor.left，直到cursor为空
3、弹出栈顶节点，打印cursor，cursor=cursor.right
4、重复2、3，直到栈和cursor均为空
```

</details>

- 后序遍历

<details>

```text
后序遍历比较复杂，需要借助2个栈来实现。
1、cursor=root，将cursor压入栈A
2、弹出A栈顶节点，将其压入栈B。将其左节点、右节点按顺序压入栈A
3、重复2，直到栈为空
```

</details>
6.

# 参考文献

1. leetcode.cn