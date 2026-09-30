Making Change Problem Using Dynamic Programming

Aim

To implement the Making Change Problem using Dynamic Programming.

Description

The Making Change Problem finds the minimum number of coins required to make a given amount.

In this program, the available coins are:

- 1
- 4
- 6

The required amount is 8.

Dynamic Programming is used to find the minimum number of coins needed.

Algorithm

1. Create a DP array where "dp[i]" represents the minimum number of coins needed to make amount "i".
2. Set "dp[0] = 0".
3. Initialize the remaining values to infinity.
4. For each amount from 1 to the required amount:
   - Check every available coin.
   - If the coin value is less than or equal to the current amount, calculate the number of coins required.
   - Store the minimum value in "dp[i]".
5. The final answer is stored in "dp[amount]".

Example

Coins = "{1, 4, 6}"

Amount = "8"

The minimum combination is:

"4 + 4 = 8"

Therefore:

Minimum number of coins = 2

Time Complexity

"O(amount × number of coins)"

Space Complexity

"O(amount)"

Language

C

Sample Output

Coins: 1 4 6
Amount: 8
Minimum number of coins required: 2