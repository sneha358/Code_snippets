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
