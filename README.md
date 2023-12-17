# Exp-3b - Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
#Program for linear search method to match the item in a list
#Developed by: P.LOKNAATH
#RegisterNumber: 23004546

def linearSearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
    
    
array = eval(input())
k = eval(input()) 
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if (result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by: P.LOKNAATH
#RegisterNumber: 23004546

def binarySearchIter(array, k, low, high):
    
    while low<=high:
        mid = low + (high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
array = eval(input())
array.sort()
k = eval(input()) 
result=binarySearchIter(array, k,0, len(array)-1)
if(result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
#Program to find the element in a list using Binary Search (recursive Method).
#Developed by: P.LOKNAATH
#RegisterNumber: 23004546

def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        
        elif arr[mid]>k:
            return BinarySearch(arr, k, low, mid-1)
        
        else:
            return BinarySearch(arr, k,mid+1, high)
    else:
        return -1
            
arr = eval(input())
arr.sort()
k = eval(input()) 
result = BinarySearch(arr, k, 0, len(arr)-1)

if(result== -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/2ac2a251-7b6a-4800-a593-63accb464ae3)
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/8ba17796-ac56-42ca-9e17-5256a5d69f2f)
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/cc52e40f-dd8c-46e5-a5f9-b216477750f0)

## Output
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/4280d79f-3981-40de-a069-201474fa5e93)
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/6a9783d3-1537-48d9-89b8-7a235938d97e)
![image](https://github.com/Loknaath-sec/Search-Algorithm/assets/145742558/5eebf54b-ae44-49c0-bcc4-97a38fcaacd2)

## Name: P. LOKNAATH
## REgister Number : 212223240080

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
