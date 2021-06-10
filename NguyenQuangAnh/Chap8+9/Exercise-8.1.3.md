*__Question:__ Write the predicate (only the predicate) to represent the requirement:*

“List all the wireless mice that either retail for more than $100 or for which the store has more than 20 items. Also list non-wireless mice that retail for more than $50.”

*__Answer:__*<br>
<br>
((wireless = true) ^ ((price > 100) v (num > 20))) ^ ((wireless = false) ^ (prive > 50))


