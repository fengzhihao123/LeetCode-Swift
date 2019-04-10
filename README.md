# LeetCode-Swift

```
//给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。

/*
 1、将数组的值和value当做key-value存放在dictionary中
 2、判断target减去当前value得到的result是否存在dictionary中
 3、若存在则代表value+result=target，则返回value和result的index
 4、若不存在则将value存入dictionary中
 */
func twoSum(_ nums: [Int], _ target: Int) -> [Int] {
    var dict = [Int: Int]()
    
    for (index, value) in nums.enumerated() {
        if let lastIndex = dict[target - value] {
            return [lastIndex, index]
        }
        dict[value] = index
    }
    return [0]
}
```
