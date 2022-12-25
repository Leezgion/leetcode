# 最长公共前缀

> 简单

编写一个函数来查找字符串数组中的最长公共前缀。

如果不存在公共前缀，返回空字符串 `""`。

##### 示例 1：

```
输入：strs = ["flower","flow","flight"]
输出："fl"
```

##### 示例 2：

```
输入：strs = ["dog","racecar","car"]
输出：""
解释：输入不存在公共前缀。
```

##### 提示：

- `1 <= strs.length <= 200`
- `0 <= strs[i].length <= 200`
- `strs[i]`仅由小写英文字母组成

## 题解

```javascript
/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function (strs) {
  const everyStrsLength = strs.map((str) => {
    return str.length;
  });
  const longestLength = Math.max(...everyStrsLength);
  let result = "";
  let letter = "";
  let mid = "";
  for (let i = 0; i < longestLength; i++) {
    letter = strs.map((str) => {
      return str[i];
    });
    mid = letter[0];
    if (letter.every((item) => item == letter[0])) {
      result += mid;
    } else {
      result += "";
      break;
    }
  }
  return result;
};
```
