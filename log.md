# 100 Days Of Code - Log

### Day 0: January 2 2017

**Today's Progress**: Reviewing on Markdown Syntax

**Thoughts** I kept putting off learning Markdown Syntax, but I finally took the time do learn it! Definetely good way to start writing for the challenge!

**Resources on Markdown**
+ [Udacity's Writing READMe's](https://www.udacity.com/course/writing-readmes--ud777)
+ [CommonMark.org](http://commonmark.org/help/tutorial/index.html)


**Today's Progress**: Algorithm on Array 3sum

**Thoughts**: Embarrassingly, I had a hard time solving this _medium_ level [3Sum Question](https://leetcode.com/problems/3sum/). Even though I was able to solve it, it was not efficient; with extra help, I learned a lot including:
+ Traversing around the Array
+ `Array.prototype.some` usage

Answer to the question:

```
var threeSum = function(nums) {
  let result = [];
  let answer;
  let target;
  if(nums.length < 3){ // if nums.length is less than 3, quit ahead
      return result;
  }
  let len = nums.length

  nums.sort( (a,b) => a-b) //SORTING helps to organize
  // console.log(nums)
  for(let i = 0; i < nums.length - 2; i++){ // you only care up to the last 3 elements in the array
    if (i === 0 || nums[i] > nums[i - 1]){  //this helps avoid any duplication

      target = 0 - nums[i];

      let j = i + 1; // traverse from left to right
      let k = len - 1 // travers from right to left

      while(j < k ){
        if(nums[j] + nums[k] === target){
          result.push([nums[i], nums[j], nums[k]]); //this is pushing new combo
          j++; // traverse to right
          k--; // traverse to left
          while(j < k && nums[j] === nums[j - 1]){j++;} //avoids any duplicates
          while(j < k && nums[k] === nums[k + 1]){k--;} //avoids any duplicates
        } else if( nums[j] + nums[k] < target){ //if the current combo is less than target, traverse to right
          j++
        } else { //if the current combo is higher than target, traverse to left
          k--;
        }
      }
    }
  }

  return result
};
```

**Today's Progress**: FCC's NightLife Coordination App

**Thoughts** Today I've completed simple LogIn/Signup/Signoff routes using JWT and Express (REST Architecture). I will need to come up with how to keep track users on which venues they are going. Cosmetics will be last to do on the list
