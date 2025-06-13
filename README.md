# wikigame
making llms play wikigame  
this is a living document that maintains the current progress

## navigation game desc

```
START → Intro Snippet → Strategic Link Choice → Next Intro Snippet → ... → TARGET
```

the agent needs to understand wikitext, identify links, and make strategic navigation decisions  
to make it financially feasible for running large-scale evaluations, only intro snippet are used currently

## progress
i have observed that the task is extremely easy for decent models if it sees the full wikitext but extremely challenging if only intro snippets are used  
using the full wikitext also means a single round will use a LOT of tokens

a good balance is if the agent has to decide, like humans might:

"Should I navigate immediately with the intro links?  
Or should I spend a turn exploring the "History" section because it might have links to related historical figures?  
Or maybe the "Geography" section has links to nearby places?"

it's like having a limited "look ahead" ability that costs a turn to use. this is what i am experimenting with next.
