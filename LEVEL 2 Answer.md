Question 1: How does parallel programming/computing works? What do you think 
will be the advantage of utilizing parallel approach?

Answer: Advantage of parallel computing. The advantages of parallel computing are that computers can execute code more efficiently,
which can save time and money by sorting through “big data” faster than ever.
Parallel programming can also solve more complex problems, bringing more resources to the table.

Question 2:
In a right triangle, the square of the length of one side is equal to the 
sum of the squares of the lengths of the other two sides. Write a 
program that prompts the user to enter the length of the three sides of 
a triangle and then outputs a message indicating whether the triangle 
is a right triangle. 

Answer: Source Code
# Programmed by: Luganob Jerald BSCS-3B

b = float(input("Enter length of Base : "))
p = float(input("Enter length of Perpendicular : "))
h = float(input("Enter length of Hypotenuse : "))

if h ** 2 == ((b ** 2) + (p ** 2)):
    print("It's a right triangle")
else:
    print("It's not a right triangle")


#Output Screenshot
1.
![2](https://user-images.githubusercontent.com/89097911/181267990-f4c2652c-1d79-44db-836a-7d34234af79f.png)
2.
![1](https://user-images.githubusercontent.com/89097911/181268000-2d2f026b-2eaa-47cb-b00a-9b55f392bdb7.png)



Question 3:
Write a program that prompts the user to input a number between 0 
and 35. If the number is less than or equal to 9, the program should 
output the number; otherwise, it should output A for 10, B for 11, C for 
12… and Z for 35. 

Answer: Source Code
#Programmed by: Luganob Jerald M. BSCS-3B

letter = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r', 's','t','u','v','w','x','w','z']
number = [10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35]

def get_index(n):
    for i in range(len(number)):
        if n==number[i]:
            return i


def get_letter(index):
    for i in range(len(letter)):
        if index==i:
            return letter[i]

N = int(input("Enter an integer between 0 and 35: "))
if N<=9:
    print(N)
else:
    index=get_index(N)
    print(get_letter(index).upper())

#Output Screenshot
1.
![2](https://user-images.githubusercontent.com/89097911/181268783-65d2e1a0-288e-46ad-b383-a0262bb5efd0.png)
2.
![1](https://user-images.githubusercontent.com/89097911/181268789-858a9452-36fd-48d8-914b-5dae3c4e4704.png)



Question 4: Write a program that will display all numbers divisible by 3, 4 and 5 from 1-50.

Answer: Souce Code
#Programmed by: Luganob Jerald M.

def result(N):
    for num in range(N):
        if num % 3 == 0 and num % 5 == 0:
            print(str(num) + " ", end="")
        else:
            pass

if __name__ == "__main__":
    N = 50
    result(N)

#Output Screenshot
![3](https://user-images.githubusercontent.com/89097911/181269137-9ef0c586-95ee-4b26-bf67-3a184db871b3.png)

