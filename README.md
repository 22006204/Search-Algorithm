# Linear Search and Binary search
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
```python
''' 
Program for linear search method to match the item in a list
Developed by: SATHISH R
RegisterNumber: 22006204
'''
def linearSearch(array,n,k):
    for i in range(0, n):
        if (array[i] == k):
            return i
    return -1
    
array = eval(input()) 
k=eval(input())
n= len(array)
array.sort()
result = linearSearch(array,n,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: SATHISH R
RegisterNumber: 22006204
'''
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid +1
        else:
            high = mid- 1
    return - 1
array = eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array,k,0,len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    

```
iii) # Find the element in a list using Binary Search (recursive Method).
```python
'''
Program to find the element in a list using Binary Search1(recursive Method)..
Developed by: SATHISH R 
RegisterNumber: 22006204
'''
def BinarySearch(array, k, low, high):
    if  high >= low:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] > k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    else:        
        return - 1
array = eval(input())
array.sort()
k = eval(input())
result = BinarySearch(array,k,0,len(array)-1)
if(result == -1):
    print(array)
    
    print("Element not found")
else:
    print(array)
    
    print("Element found at index: ",result)

```
## Input and Output
![li2](https://user-images.githubusercontent.com/118787261/214855083-610a5af1-fd9d-4dbf-9da1-676c063d59f1.png)
![li3](https://user-images.githubusercontent.com/118787261/214855104-e2881476-79bc-46e8-96f2-dca54425ea34.png)
![li4](https://user-images.githubusercontent.com/118787261/214855108-1e5f0abd-5924-4a78-a597-c2d086e8ba37.png)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
