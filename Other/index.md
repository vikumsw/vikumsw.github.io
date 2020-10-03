---
layout: page
title: Problem Solving
# tags: [satwik, kottur, contact, graduate, cmu]
# modified: 2014-08-08T20:53:07.573882-04:00
comments: false
--- 

<p style="text-align: left;">I absolutely love problem solving. I find solving algorithms, puzzles and riddles&nbsp;highly engaging.&nbsp;Below are a small collection of diversions that I find interesting, usually because their solutions are creatively simple.</p>

<h2 style="text-align: left;"><strong>Algorithm Challenges</strong></h2>
<table border="1" style="border-collapse: collapse; width: 100%;">
<tbody>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">1</td>
<td style="width: 89.422%; height: 21px; border-style: solid;"><b>Count the Islands: </b><span>Given a matrix of 1s and 0s, return the number of "islands" in the matrix. A 1 represents land and 0 represents water, so an island is a group of 1s that are neighboring whose perimeter is surrounded by water. For example, this matrix has 4 islands.</span><br />
<span>1 0 0 0 0</span><br /><span>0 0 1 1 0</span><br /><span>0 1 1 0 0</span><br /><span>0 0 0 0 0</span><br /><span>1 1 0 0 1</span><br /><span>1 1 0 0 1</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/Solutions/CounttheIslands.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">2</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>String of Parentheses: </b>
<span>Given a string of parentheses, write a function to compute the minimum number of parentheses to be removed to make the string valid (i.e. each open parenthesis is eventually closed).</span></td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/Solutions/StringofParentheses.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">3</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Can you make a palindrome from a given string: </b>
<span>Given a string, determine whether any permutation of it is a palindrome. For example, carrace should return true, since it can be rearranged to form racecar, which is a palindrome. daily should return false, since there's no rearrangement that can form a palindrome.</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/CanMakePalindrome.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">4</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Smallest Sparse Number: </b>
<span>We say a number is sparse if there are no adjacent ones in its binary representation. For example, 21 (10101) is sparse, but 22 (10110) is not. For a given input N, find the smallest sparse number greater than or equal to N. Do this in faster than O(N log N) time.</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/smallestSparseNumber.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">5</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Max & Min: </b>
<span>Given an array of numbers of length N, find both the minimum and maximum using less than 2 * (N - 2) comparisons.</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/maxMinFind235.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">6</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Maximum Subarray Sum of a Circular Array: </b>
<span>Given a circular array, compute its maximum subarray sum in O(n) time. A subarray can be empty, and in this case the sum is 0. For example, given [8, -1, 3, 4], return 15 as we choose the numbers 3, 4, and 8 where the 8 is obtained from wrapping around. Given [-4, 5, 1, 0], return 6 as we choose the numbers 5 and 1.</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/LargestSubArray.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">7</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Sherlock and Anagrams: </b>
<span><a href="https://www.hackerrank.com/challenges/sherlock-and-anagrams/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/C%2B%2B/sherlock-and-anagrams.cpp"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">8</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Hash Tables: Ransom Note: </b>
<span>Harold is a kidnapper who wrote a ransom note, but now he is worried it will be traced back to him through his handwriting. He found a magazine and wants to know if he can cut out whole words from it and use them to create an untraceable replica of his ransom note. The words in his note are case-sensitive and he must use only whole words available in the magazine. He cannot use substrings or concatenation to create the words he needs.

Given the words in the magazine and the words in the ransom note, print Yes if he can replicate his ransom note exactly using whole words from the magazine; otherwise, print No.

For example, the note is "Attack at dawn". The magazine contains only "attack at dawn". The magazine has all the right words, but there's a case mismatch. The answer is "No".
<br><a href="https://www.hackerrank.com/challenges/ctci-ransom-note/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/C%2B%2B/ctci-ransom-note.cpp"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">9</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Minimum Swaps 2: </b>
<span>You are given an unordered array consisting of consecutive integers [1, 2, 3, ..., n] without any duplicates. You are allowed to swap any two elements. You need to find the minimum number of swaps required to sort the array in ascending order.
<br><a href="https://www.hackerrank.com/challenges/minimum-swaps-2/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/C%2B%2B/minimum-swaps-2.cpp"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">10</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>New Year Chaos: </b>
<span>It's New Year's Day and everyone's in line for the Wonderland rollercoaster ride! There are a number of people queued up, and each person wears a sticker indicating their initial position in the queue. Initial positions increment by 1 from 1 at the front of the line to at the back.

Any person in the queue can bribe the person directly in front of them to swap positions. If two people swap positions, they still wear the same sticker denoting their original places in line. One person can bribe at most two others. For example, if n=8 and person 5 bribes person 4, the queue will look like this: 1,2,3,5,4,6,7,8.

Fascinated by this chaotic queue, you decide you must know the minimum number of bribes that took place to get the queue into its current state!
<br><a href="https://www.hackerrank.com/challenges/new-year-chaos/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/java/NewYearChaos.java"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">11</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Two Strings: </b>
<span>Given two strings, determine if they share a common substring. A substring may be as small as one character. For example, the words "a", "and", "art" share the common substring "a". The words "be" and "cat" do not share a substring.
<br><a href="https://www.hackerrank.com/challenges/two-strings/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/C%2B%2B/TwoStrings.cpp"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">12</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Array Manipulation: </b>
<span>Starting with a 1-indexed array of zeros and a list of operations, for each operation add a value to each of the array element between two given indices, inclusive. Once all operations have been performed, return the maximum value in your array.
<br><a href="https://www.hackerrank.com/challenges/crush/problem">Read the problem in Hacker Rank</a></span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/C%2B%2B/Array%20Manipulation.cpp"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">12</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Super Palindromes: </b>
<span>Let's say a positive integer is a superpalindrome if it is a palindrome, and it is also the square of a palindrome. Now, given two positive integers L and R, return the number of superpalindromes in the inclusive range [L,R].</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/SuperPalindrome.py"><strong>Code</strong></a></td>
</tr>
<tr style="height: 21px;">
<td style="width: 1.61765%; height: 21px; border-style: solid;">13</td>
<td style="width: 89.422%; height: 21px; border-style: solid;">
<b>Moving Robot: </b>
<span>On a infinite plane, a robot initially stands at (0,0) and faces north. The robot can recieve one of three insructions: 'G': go straight 1 unit.
'L': turn 90 degrees to the left.
'R': turn 90 degrees to the right.
The robot performs the instructions given in order, and repeats them forever.
return true if there exists a circle, in the plane such that the robot never leaves the circle.

Input: "GGLLGG". Ouput: True</span>
</td>
<td style="width: 13.5037%; height: 21px; border-style: solid;"><a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving/blob/master/src/main/python/IsLooping.py"><strong>Code</strong></a></td>
</tr>
</tbody>
</table>
<p>More fun algorithm problems with answers can be found here in this <a href="https://github.com/vikumsw/Algorithms_For_Problem_Solving">repository</a>.</p>

<h2 style="text-align: left;">Fun Puzzles</h2>

<table border="1" style="border-collapse: collapse; width: 100%;">
<tbody>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">1</td>
<td style="width: 97.8212%; height: 20px;"><b>The Following Cars:<span>&nbsp;</span></b><span>Four cars that all move with the same speed of 60 mph start off at the four corners of a square of side 1 mile. Label the cars in clockwise order 1,2,3,4. At every instant, car 1 moves in the direction of car 2, car 2 in the direction of car 3, car 3 in the direction of car 4 and car 4 in the direction of car 1. Where will the cars eventually meet and how far will each car have travelled</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">2</td>
<td style="width: 97.8212%; height: 20px;"><b>The Monty Hall Problem:<span>&nbsp;</span></b><span>There are 3 doors, behind one of which is a prize. You pick a door and I am forced to show you a vacant door (other than the one you picked). I now give you the option to switch to the remaining door. Do you definitely want to switch, definitely not want to switch or does it matter whether you switch or not.</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">3</td>
<td style="width: 97.8212%; height: 20px;"><b>Counting the 1s:</b><span>&nbsp;Among the integers from 0 to 10,000,000,000 do the majority of them contain a 1?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">4</td>
<td style="width: 97.8212%; height: 20px;"><b>Got Gas?</b><span>&nbsp;On a circular circuit around the city, there are fuel stations. All the fuel in these stations is just enough to complete one circuit around the city. Is it always possible to start at one of the stations with an empty tank and complete one full circuit without running out of fuel?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">5</td>
<td style="width: 97.8212%; height: 20px;"><b>Leaving the Grounds</b><span>&nbsp;You are at the center of a circular field with radius 1 mile. A guard dog is restricted to run around the perimeter. You run at 10mph and the dog at 40mph. Your goal is to escape from the field, and the dog will try its best to stop you. Can you escape?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">6</td>
<td style="width: 97.8212%; height: 20px;"><b>The Scared Guards:</b><span>&nbsp;57 security guards are positioned so that no two pairs of guards are the same distance apart. Every guard watches the guard closest to him. Is there an arrangement of the guards so that every guard is being watched?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">7</td>
<td style="width: 97.8212%; height: 20px;"><b>4 Men and a Flashlight:</b><span>&nbsp;4 men arrive at a bridge in the dark, with one flashlight. The flashlight is required by any group crossing the bridge, and the bridge can only hold two men at a time. The minimum times it takes for the men to walk across the bridge are 1,2,5,10 minutes respectively. What is the minimum time by which all 4 men can have crossed the bridge?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">8</td>
<td style="width: 97.8212%; height: 20px;"><b>Maximizing the Probability:</b><span>&nbsp;You are given 50 white marbles and 50 black marbles along with two jars. You are asked to place all 100 marbles into the jars in any way you choose. Afterwards, you will be blindfolded, the jars will be shaken and rearranged, and you will be asked to select one marble from either jar. How would you arrange the marbles originally to maximise the probability of drawing a white marble?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">9</td>
<td style="width: 97.8212%; height: 20px;">
<b>100 Prisoners with Red/Black Hats</b><span>&nbsp;100 prisoners in jail are standing in a queue facing in one direction. Each prisoner is wearing a hat of color either black or red. A prisoner can see hats of all prisoners in front of him in the queue, but cannot see his hat and hats of prisoners standing behind him.The jailer is going to ask color of each prisoner&rsquo;s hat starting from the last prisoner in queue. If a prisoner tells the correct color, then is saved, otherwise executed.&nbsp;<b>How many prisoners can be saved at most</b>&nbsp;if they are allowed to discuss a strategy before the jailer starts asking colors of their hats.</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">10</td>
<td style="width: 97.8212%; height: 20px;"><b>Ratio of Boys and Girls in a Country where people want only boys</b><span>&nbsp; In a country, all families want a boy. They keep having babies till a boy is born. What is the expected ratio of boys and girls in the country?</span>
</td>
</tr>
<tr>
<td style="width: 2.17876%;">11</td>
<td style="width: 97.8212%;"><b>2 Eggs and 100 Floors:</b><span>&nbsp; Suppose that we wish to know which stories in a 100-story building are safe to drop eggs from, and which will cause the eggs to break on landing. What strategy should be used to drop eggs such that total number of drops in worst case is minimized and we find the required floor.</span></td>
</tr>
<tr>
<td style="width: 2.17876%;">12</td>
<td style="width: 97.8212%;"><b>10 Coins Puzzle:</b><span>&nbsp;You are blindfolded and 10 coins are place in front of you on table. You are allowed to touch the coins, but can&rsquo;t tell which way up they are by feel. You are told that there are 5 coins head up, and 5 coins tails up but not which ones are which. Can you make two piles of coins each with the same number of heads up? You can flip the coins any number of times.</span>
</td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">13</td>
<td style="width: 97.8212%; height: 20px;"><b>A King, 1000 Bottles of Wine, 10 Prisoners and a Drop of Poison:</b><span>&nbsp;The King of a small country invites 1000 senators to his annual party. As a tradition, each senator brings the King a bottle of wine. Soon after, the Queen discovers that one of the senators is trying to assassinate the King by giving him a bottle of poisoned wine. Unfortunately, they do not know which senator, nor which bottle of wine is poisoned, and the poison is completely indiscernible. However, the King has 10 prisoners he plans to execute. He decides to use them as taste testers to determine which bottle of wine contains the poison. The poison when taken has no effect on the prisoner until exactly 24 hours later when the infected prisoner suddenly dies. The King needs to determine which bottle of wine is poisoned by tomorrow so that the festivities can continue as planned. Hence he only has time for one round of testing. How can the King administer the wine to the prisoners to ensure that 24 hours from now he is guaranteed to have found the poisoned wine bottle?</span></td>
</tr>
<tr style="height: 20px;">
<td style="width: 2.17876%; height: 20px;">14</td>
<td style="width: 97.8212%; height: 20px;"><a href="https://mindyourdecisions.com/blog/2016/03/20/the-seemingly-impossible-escape-sunday-puzzle/"><b>The Seemingly Impossible Escape</b></a>
</td>
</tr>
</tbody>
</table>
<br>
<p>Above are few puzzels I really liked solving. Please feel free to contact me if you like to discuss solutions to above puzzles. I really love to know how you solved them</p>
