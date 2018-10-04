# Answers #
1. #### What teams at Vineti are you interested in and why? (Dev or QA) ####
I think Software Development is a great career choice .It is very attractive for me ,because there is nothing more satisfying than solving a problem that has not been  solved yet by anyone else.
As a software developer I can create new systems , can give creative and  unique solutions to many problems .It will give me opportunity do not stay in the same place . So I am sure that I will get pleasure from my work.
2. #### What is your favorite programming language and why? ####
I prefer coding in c++ ,because it is convenient for me .Due to the fact that I started programming from c++ ,now I am learning other languages more easily  and effectively .
3. #### What is a Linked list ? ####
Linked list is one of  the most common data  structures .
It is  a linear data structure  ( elements of list we  will call nodes ). Each node contains  data and points to the next node  of the list.The last node points to null.
Advantages.In linked list elements can be easily inserted or removed without redistribution  of the entire structure.
Disadvantages.
More memory is required to store elements in linked list as compared to array, because in linked list each node contains a pointer .
We can not randomly access any element as we do in array by index.So if we want to
access an element in position n we can not directly apply to the n-th node.
4. #### You work in an ice cream shop and step into the back for a few minutes. You return and see a large group of people waiting. How would you serve them? ####

	I will serve them in turn .So the person who has waited  longer than others,he(she) will get the ice-cream the earliest .And if my ice-cream machine allows me I will save time in this way. Lets assume that one ice-cream have been made in two minutes.I will make two different ice-creams together.For example you want chocolate ice-cream and your friend wants vanilla ice-cream .SO i can give you and your friend your ice-creams in 2 minutes instead of 4 minutes.
5. #### How would you test a pen? ####
Saying test a pen I understand I have to know if pen is writing ,what is the color of it ,is it suitable for me and so on .All this characteristics I  can test with writing something on paper.
6. ####  As a test engineer in Amazon what would you test first (assuming authentication functionality is already covered)? ####
I will test components of a project.  My work will include  writing tests,building testing infrastructure, collecting and reporting on testing metrics, participating in product design meetings etc. I need the skills like  strong coding, design and analytic thinking .
7. #### You have a list of numbers from one to one million and there is a missing number. How would you find the missing number? ####


  ```c++
  int FindMissingNumber (int a [],int n )
  {
	int s = 0;
    int k = (  n + 1 ) * ( n + 2 ) / 2;
	for (int i = 0; i < n; ++i)
		s += a[i] ; //sum of numbers of array
	return (k - s);
}
```
8. #### How would you determine the angle between the hour-hand and minute-hand of a clock at 3:20? ####
In one hour the hour-hand draws 30 degree bow ,because there are 12 hours in one day. So we can easily calculate it dividing 360 by 12.But  hour-hand has not drawn 30 degree yet because in this case only 20 minutes  are passed which is equal to one third of an hour .So the hour-hand has drown 30*1/3=10 degree bow .As we  know that the hour-hand has drown 30 degree bow ,and the minute-hand is on the number 4 ,we can calculate the angle between the hour-hand and the minute-hand by subtracting 30-10=20 .
9. #### How would you determine if a number is a power of two? ####
``` c++
bool PowerOFtwo(int n)
{
    int m=n-1;
    return !(n & m);  
}
```
10. #### How would you remove duplicates from a list? ####
``` c++
void removingNumber(int numbers[], int ind, int &size)
{
	int i;
	for (i = ind; i < size - 1; i++)
		numbers[i] = numbers[i + 1];
	size--;
}

void removingDuplicate(int numbers[], int &size)
{
	int i, j;
	int num;
	for (i = 0; i < size; i++)
	{
		num = numbers[i];
		for (j = i + 1; j < size; j++)
		{
			if (num == numbers[j])
			{
				removingNumber(numbers, j, size); j--;
			}
		}
	}
}
```
11. #### How would you determine if a string has all unique characters? ####
``` c++
bool IsUnique(string myString)
{
	for (int i = 0; i < myString.length(); i++)
		for (int j = i + 1; j < myString.length(); j++)
			if (myString[i] == myString[j])
				return false;
	return true;
}
```
12. #### How would you reverse a string? ####
```c++
void String(string& myString)
{
	char a;
	for (int i = 0; i <myString.size() / 2; i++)
	{
		a = myString[i];
		myString[i] = myString[myString.size() - i - 1];
		myString[myString.size() - i - 1] = a;
	}
}
```
13. #### How would you compress a string such that 'AAABCCDDDD' becomes 'A3BC2D4'? Only compress the string if it saves space. ####
``` c++
void CompressString(string& myString)
{
	string nStr;
	char a;
	int i = 0;
	int j = 0;
	while (i < myString.size())
	{
		j = 0;
		a = myString[i];
		nStr += myString[i];
		while (a == myString[i])
		{
			j++;
			i++;
		}
		if (j != 1)
			nStr += j+'0';
	}
	myString = nStr;
}
```
14. #### Given an array of 0's and 1's, how would you move all of the 0's to the beginning of the array and all of the 1's to the end of the array? ####
``` c++
void sortingArrayFunction(int* arr,int n)
{
    int i=0, j=n-1;
    while(i!=j)
    {
        if(arr[i]==1 && arr[j]==0)
          {
              arr[i]=0;
              arr[j]=1;
              i++;j--;
            }
        else
        {
            if(arr[i]==0)
            i++;
            if(arr[j]==1)
            j--;
        }
    }
}
```
15. #### How would you design a vending machine or a toaster? ####
First I have to know what amount of money I need to design toaster.I need to know the size of the toaster.I will get the answers of this questions
How does it work? Is it timer based or manual toaster?
How many years of guarantee it has?
How much power limit does it operate ? 

16. #### You have two light bulbs at a 100-story building. You want to find the lowest floor at which the bulbs will break when dropped. How would you find the floor using the least number of drops?####
First light bulb we  drop from 16-th floor .If it breaks ,we will search the floor between 1 and 16 .So in the worst case we drop 16 times . If we drop the light bulb from 16-rd floor and it does not break we drop it from 31-st floor(16+15).If it breaks ,we will search the floor between 17 and 31.Since we have  already dropped the bulb from 16rd floor ,the count of the throws in the worst case is equal to 16 (15+1).If it does not break we will drop it from 45-th(16+15+14)floor. If it breaks ,we will search the floor between 31 and 45 .Since we have  already dropped the bulb from 16th and 31-st
 floors ,the count of the throws in the worst case is equal to 16 (14+1+1).Then we continue this process dropping  it from 58-th,70-th,81-st,91-st,100 floors .In any Case the maximum count of throwing is equal to 16.
17. #### If you have a square room with no roof, and you had four pillars you had to plant on the walls so that each pillar touched two walls, how would you do it? ####
I denote with x the side of roof square.
In the roof square I   embrace  a square which is consisted of pillars (the length of the sides of this square are equal to x*sqrt(2)/2).The peaks of this square are the midpoints of the roof square sides .So we have a square on the walls of room ,which is put in the roof square and its each side touches two walls.


18. #### Given 9 balls all of which weigh the same except for one, what is the minimum of weighings necessary to find the ball weighs more (or less)? ####
I denote with X he ball weigh  of which is not equal to weight of others.
I will separate from  them 3 groups .In each group we have 3 balls.

Steps.

1)weight first and second groups of balls
There are  2 variants.

variant 1

Their weights are equal , so X is in the 3rd group.
2)I will weight second and third groups to know  whether the weight of X is more or less than others .

3)Then I will weight any two balls of 3rd group .The X is The ball which has more (less) (it is connected with previous step) weight than others .

variant 2

1)If the weight of the first group is more(less) than the weight of the second group.

2)I will weight the first(second) and third groups.
3) If their weights are equal , X is in the second(first )group and its weight is less (more ) than others weight( it is connected with the previous step).Then I will weight any 2 balls of the second ( first) group .X is the ball which weight is less (more) than others.

4) If the weight of the first(second) group is more than the third groups weight ,X is in the first(second) group and the weight of X is more (less) than others weight .Then I will weight any 2 balls of the first group .X is the ball which weight more (less)than the weight of others.
So we can do  minimum 3 weightings for solving this problem.
19. #### How would you solve the N Queens problem? [Bo+nus] ####
20. #### How would you find the longest palindrome in a string? [Bonus] ####
