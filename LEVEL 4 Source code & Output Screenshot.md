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
