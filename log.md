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


### Day 1: January 3 2017

**Today's Progress**: Working on FCC's Nightlife Coordination App

**Thoughts** Today I've felt I made many progress. I am very close to finishing the overall functunality including
+ As an unauthenticated user, when I login I should not have to search again.
+ As an authenticated user, I can add myself to a bar to indicate I am going there tonight
+ As an authenticated user, I can remove myself from a bar if I no longer want to go there.

However I made the following progress:
1. Active Tabs are working properly when re-rendering the pages
2. Users can see if they are logged in or not via Materialice's CSS
3.  Users's database are updated when they make search


### Day 2: January 4th 2017

**Today's Progress**: Working on FCC's Nightlife Coordination App

**Thoughts**: Though relatively simple I've completed one of the user stories':
+ As an unauthenticated user, when I login I should not have to search again.


Unfortunately today marks my last say in Florida to spend my time with them. Back to CA! I am hoping to finish the rest of the functunality by the end of this week!

### Day 3: January 5th 2017

**Today's Progress:** Working on FCC's Nightlife Coordination App

**Thoughts**: I made progress on how to implement logically on how to keep track of other user's RSVP, as well as the current user's RSVP. I spent my coding during my time flying from Florida to California. Jet lag is kicking soon...

### Day 4th: January 6th 2017

**Today's Progress:** Resume 2017

**Thoughts**: I finally updated my resume for 2017. It's amazing that looking back from my 2016 resume, I learned a lot of technologies :)

**Today's Progress:** Working on FCC's Nightlife Coordination App

**Thoughts**: Unfortunately I did make any progress, other than refactoring the logic of keeping track of users without using React-Form. Spent most of the day working on my resume :-)

### Day 5th: January 7th 2017

**Today's Progress:** Working on FCC's Nightlife Coordination App

**Thoughts**: Good news everyone! I finished 85% with the Nightlife App! Now it needs some debugging and cosmetic layouts :)

### Day 6th: January 8th 2017

**Today's Progress:** Working on FCC's Nightlife Coordination App

**Thoughts**: Promise, promise... more promise!!

### Day 7th: January 9th 2017

**Today's Progress:** Working on FCC's Nightlife Coordination App

**Thoughts**: Officially done with the app! It can now show list of guests via modal and keep track of current users' RSVP. Now onto CSS and aesthetic ;)
