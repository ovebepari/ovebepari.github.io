---
layout: post
title: I might have found some bug in Craftsmen's recent online screening test problemset! 
description: The generated input for the participents might have been judged wrongly! 
image: /post_images/2022/craftsmen_docker_artifacts.png
comments: false
categories: Interview-Experiences 
location: DUET, Bangladesh
---

TLDR; <a href="https://craftsmenltd.com/">Craftsmen</a> asked us to find the maximum depth of a bracket sequence, provided sequence can be valid or invalid, however, our answers were checked with a code that only works for valid sequences. I can tell because we were provided a docker image and I could see the server code!

I extracted the artifacts from the docker image:

![Craftmen's docker artifacts](/post_images/2022/craftsmen_docker_artifacts.png){:.center-image}

Craftsmen's problem statement as seen:
> You need to find the maximum depth of nested angular brackets in this problem string. For example the maximum depth for this < <<>> <<>> > is three. The maximum depth of <<><><<<>>><<>>> is four. You need to write a small function to find out the maximum depth of the string as can be found in the problem property of this JSON object.

The server code which checks our answer, to find the maximum depth of a bracket sequence from the `problemUtils.ts` file: 

```typescript
export const maxDepth = (s: string): number => {
  let count = 0;
  const st = [];

  for (let i = 0; i < s.length; i++) {
    if (s[i] == '<') st.push(i); // pushing the bracket in the stack
    else if (s[i] == '>') {
      if (count < st.length) count = st.length;
      // keeping track of the parenthesis and storing
      // it before removing it when it gets balanced
      st.pop();
    }
  }

  return count;
};
```
Which is a solution of a famous leetcode problem <a href="https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/">maximum nesting depth of the parentheses - Leetcode </a>, and it will work and only work for valid bracket/parentheses sequences, clearly stated on the leetcode problemset.

The server generated bracket sequences, in a simple enough pattern, x opening brackets (depending on user email) followed by exactly 6 closing brackets, repeated hundreds of times. The number of opening and closing brackets are not the same and it is not a valid bracket sequence! So our anwers were judged by a wrong server code!

This server code fails for this corner case, <a href="https://www.typescriptlang.org/play?#code/AQYw9gdgzgLsC2BDAHgEQKYAcYAtgF5gAKKALmFgCcBLCAcwEpyIBXeAI3UoID5gBvAFDBgAG3RxwLCHEIAGANzDQkWBVnAA2gF0lygGZhuRcXGoFgi4OYA8FAHTj6uBdYDUbhgOUjq+4lCa1NoEhADkNmFesPaYLFA4RNQMrgD0qcBxCbR0wLjowOyUiCAA1hLWEHk4BbAlpT7A6KJQBX4BQSH44TxR3iID1v5EUjLAdjFOdLheoxqT6M44SoMi6cDlWDl5xWXAYP75mYiUi-lQ1FDAiBAAJupGOY1rGdRwnIanwKfwYABu2zewAA7jUqkC6BIruxEKIbiB0LdnupYmBMEQUo0AL7KHHKU4wFiUKpzJRYvTgaBgcSOMB0IgAIiQaCwuHIDOAbgQKAw2ESDJsgsFPAZDExQA"> "play here" </a>:
```
input: <<<<<>
server ans: 5
valid ans: 1
```

I spent hours to pass this step 1, solving for corner cases, I emailed that there might be something wrong in the server code during the test, turned out I was correct. I got rejected today for taking a long time to solve these problems though, I had to guess the server might be expecting a solution for a valid string!