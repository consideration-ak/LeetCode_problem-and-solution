![](https://github.com/Zhenghao-Liu/LeetCode_problem-and-solution/blob/master/0031.下一个排列/31.下一个排列英文题目.jpg)
`
介于题目有点难读懂翻译一下  
先找出最大的索引k满足nums[k] < nums[k+1],如果不存在,就翻转整个数组,结束;  
再找出另一个大于K且为最大的l，满足nums[k] < nums[l];  
交换nums[l]和nums[k];  
最后翻转nums[k+1:]  
举个例子:
比如nums = [1,2,7,4,3,1],下一个排列是什么?
找到第一个最大索引是nums[1] = 2
再找到第二个最大索引是nums[5] = 3
交换,nums = [1,3,7,4,2,1];
翻转,nums = [1,3,1,2,4,7]
`


实现获取下一个排列的函数，算法需要将给定数字序列重新排列成字典序中下一个更大的排列。

如果不存在下一个更大的排列，则将数字重新排列成最小的排列（即升序排列）。

必须原地修改，只允许使用额外常数空间。

以下是一些例子，输入位于左侧列，其相应输出位于右侧列。
```
1,2,3 → 1,3,2
3,2,1 → 1,2,3
1,1,5 → 1,5,1
```

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/next-permutation
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
