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
```

##  2553. Separate the Digits in an Array.eg 12,33==1,2,3,3

```cpp
 vector<int> separateDigits(vector<int>& nums) {
        vector<int> answer;
        int n= nums.size();
        for(int i=0; i<n; i++){
            vector<int> temp;

            while(nums[i]>0){
                temp.push_back(nums[i]%10);
                nums[i]=nums[i]/10;
            }
            reverse(temp.begin(),temp.end());
            for(int x=0;x<temp.size();x++){
            answer.push_back(temp[x]);
            }
        }
        
        return answer;
    }
```
