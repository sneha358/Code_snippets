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

## linklist traverse
```cpp
  ListNode* temp = head;
        while(temp!= NULL){
            cout<<temp->val<<" ";
            temp= temp->next;
        }
 ```
## array to integer number basic
```cpp
int array_to_int(vector<int> v, int rflag) {
    int val = 0;
    
    if (rflag) {
        /* generating number in reverse*/
        for (int i = v.size() - 1; i >= 0; i--) {
            val = val *10 + v[i];
        }
        
    }else {
        /* generating number */
        for (int i = 0; i < v.size(); i++) {
            val = val *10 + v[i];
        }
    }
    return val;
}

int main() {
    std::cout << "Hello World!\n";
    int key = 1234;
    int tmp = key;
    int d = 0;
    int rkey = 0;
    
    while(tmp) {
        /*number to digits*/
        d =  tmp %10;
        tmp /= 10;
        
        /*digits to number*/
        rkey = rkey* 10 + d;
    }
    
    std::cout<< key <<" " << rkey<<std::endl;
    
    std::vector<int> v = {1, 2, 3, 4};
    
    std::cout<<"normal int : "<< array_to_int(v, 0) <<std::endl;
    std::cout<<"reverse int : "<< array_to_int(v, 1) <<std::endl;
    
}


## character count using array
```cpp
string data = "hello world how are you";
    vector<int> letter_count(26, 0);
    
    for(int i = 0; i < data.size(); i++) {
        if(data[i] == ' ') continue;
        int index = data[i] - 97;
    
        letter_count[index] = letter_count[index] + 1;   
    }
    
    for(int i = 0; i < data.size(); i++) {
       cout << letter_count[i] <<endl;
    }    
``
