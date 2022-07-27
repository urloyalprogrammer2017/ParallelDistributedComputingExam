1. Write a program that will generate 100 3-digit random numbers and 
store it in a list. The program should display the following: 
a. All elements in the list 
b. All numbers grouped by odd and even numbers 
c. All numbers divisible by 9. 
d. All prime numbers 
e. All numbers that contains the digit 9 (e.g 29, 91, 393, 961) 

Answer: Source with Output Screenshot


#Programmed by: Luganob Jerald M. BSCS-3B

import random

# generate 100 number 3 digit random number store in a list
gen = [random.randrange(1, 100) for i in range(3)]

# Converting list into integer
s = [str(integer) for integer in gen]
a_string = "".join(s)
res = int(a_string)

# printing all elements for gen variable
print("A. All elements in the list:", (s))

# Getting even numbers
def get_even_numbers(gen):
    even_numbers = []

    for number in gen:
        if number % 2 == 0:
            even_numbers.append(number)

    return even_numbers

# Getting odd numbers
def get_odd_numbers(gen):
    odd_numbers = []

    for number in gen:
        if number % 2 == 1:
            odd_numbers.append(number)

    return odd_numbers

print("\nB. Group of even numbers:", get_even_numbers(gen))
print("Group of odd numbers:", get_odd_numbers(gen))

# Getting elements divisible by 9 in ramdom number 100 range(3)
result = list(filter(lambda x: (x % 9 == 0), gen))
print("\nC. Numbers divisible by 9 in a list:", result)

# Getting prime elements in ramdom number 100 range(3)
def checkPrime(number):
    if number == 0 or number == 1:
        return 0
    for i in range(2, number // 2 + 1):
        if number % i == 0:
            return 0
    else:
        return number

#Main code
if __name__ == "__main__":
    ansList = list(map(checkPrime, gen))
    if sum(ansList):

        print("\nD. Prime Number : ", end="-> ")
        for ans in ansList:
            if ans:
                print(ans, end=", ")

    else:
        print("\nD. No any number from the given list is Prime")


# All numbers that contains the digit 9
print("\nE. The original list is : " + str(gen))
contain = 9

res = [ele for ele in gen if str(contain) in str(ele)]
print("Elements with digit 9: " + str(res))


#Output Screenshot
1.
![2](https://user-images.githubusercontent.com/89097911/181309809-29ceaf11-1d26-4cd8-958c-c538df6915d0.png)
2.
![1](https://user-images.githubusercontent.com/89097911/181309820-08329bf0-592d-4790-8f0b-d6dcca0bd2ad.png)


2. Given a linked list of size K, your task is to complete the function 
sum_of_lastN_nodes(), which should return the sum of last N nodes 
of the linked list. The function takes two arguments as input, the 
reference pointer of the head of the linked list and the integer N. 
Example: 
5->10->6->4->1->12 
N = 3 
sum_of_lastN_nodes(6, N) 
Output: Sum of last three nodes in the linked list is 4 + 1 + 12 = 15.


Answer: Source Code & Output Screenshot


# Programmed by: :Luganob, Jerald M.

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


head = None
n = 0
sum = 0

def push(head_ref, new_data):
    global head
    new_node = Node(0)
    new_node.data = new_data
    new_node.next = head_ref
    head_ref = new_node
    head = head_ref

def sumOfLastN_Nodes(head):
    global sum
    global n

    if (head == None):
        return

    sumOfLastN_Nodes(head.next)

    if (n > 0):
        sum = sum + head.data
        n = n - 2

def sumOfLastN_NodesUtil(head, n):
    global sum

    # if n == 0
    if (n <= 0):
        return 0

    sum = 0
    sumOfLastN_Nodes(head)
    return sum



head = None

# create linked list 5, 10, 6, 4, 1, 12
push(head, 5)
push(head, 10)
push(head, 6)
push(head, 4)
push(head, 1)
push(head, 12)

n = 3
print("Sum of last ", n,  " nodes = ", sumOfLastN_NodesUtil(head, n))

#Output Screenshot
![1](https://user-images.githubusercontent.com/89097911/181318052-b8823db6-00bf-458b-9720-c8f184862c34.png)
