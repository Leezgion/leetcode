#  两数之和 
>简单

给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 target  的那 两个 整数，并返回它们的数组下标。

你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。

你可以按任意顺序返回答案。

##### 示例1：
```
输入：nums = [2,7,11,15], target = 9
输出：[0,1]
解释：因为 nums[0] + nums[1] == 9 ，返回 [0, 1] 。
```
##### 示例2：
```
输入：nums = [3,2,4], target = 6
输出：[1,2]
```
##### 示例3：
```
输入：nums = [3,3], target = 6
输出：[0,1]
```
##### 提示：
* `2 <= nums.length <= 104`
* `-109 <= nums[i] <= 10`
* `-109 <= target <= 109`
* **只会存在一个有效答案**


## 题解
```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    let x;
    let y;
    let arr = [x, y];
    for (x = 0; x < nums.length; x++) {
        for (y = x + 1; y < nums.length ; y++) {
            if (nums[x] + nums[y] == target) {
                arr[0] = x;
                arr[1] = y;
            }
        }
    }
    return arr;
};
```
```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for(let i=0;i<nums.length-1;i++){
        for(let j=i+1;j<nums.length;j++){
            if(nums[i]+nums[j]==target){
                return [i,j]
            }
        }
    }
};
```
```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    nums.map((num,a)=>{
        const result=target-num
        for(let b=a+1;b<nums.length;b++){
            if (result==nums[b])
            return c=[nums.indexOf(num),b]
        }
    })
    return c
};
```
```javascript
```