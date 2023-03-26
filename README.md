# Code_snippets

## Count Number of Digits
```python
def number_of_digits(x):
  count = 0
  while (x > 0):
    x = x // 10
    count+=1
  return count
```

## count consecutive onse
```python
def findMaxConsecutiveOnes(self, nums: List[int]) -> int:
        gcount = 0
        count = 0
        for x in nums:
            if x == 1:
                count +=1
                if count > gcount:
                    gcount = count
            elif x == 0:
                
                count = 0
            else:
                pass
        return gcount
```
## 561. Array Partition

make n pairs (a1, b1), (a2, b2), ..., (an, bn) such that the sum of min(ai, bi) for all i is maximized. Return the maximized sum.
```cpp
int sum=0;
        sort(nums.begin(),nums.end());

        for(int i=0; i<nums.size(); i++){
            if(i%2=0){
                sum=sum+nums[i];
            }
        }
        return sum;
