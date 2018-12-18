# Introduction to Python_Python Basics                     
## Basic Manipulations on the Lists:          
```python
x = ["a", "b", "c", "d"]
print(x[1] + x[3])
```
To create the an areas-list and make some basic computing            
```python
areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]
eat_sleep_area = areas[3] + areas[7]
print(str(eat_sleep_area))
```
You know that in python when slicing a sub-list, like x[start:end], the element with the index end would not be included:           
```python
x = [1,2,3,4]
y = x[0:3]
# y = [1,2,3]
```
If we donnot specify the starting index, the execution would start from the first element, with similarity to the ending index related the last element.                   
                 
Before introducing some more general manipulations on the lists, I would like to explore more behind the scenes, which would help us understand how Python lists actually work. When we create a list x as below, an 'address' of the list would be stored in the computer memory and 'x' would contain a reference to the list, rather that containing all the elements of the list. For basic operations, the difference is not that important, but it becomes more so when we start copying lists.                
```python
x = ["a", "b", "c"]
y = x
y[1] = "z"
```
When we change the elements of y[1] as z, the corresponding element of the original list x has also changed. That's because when we copy the original list x to y with the equal sign, we just copy the reference of x to y, not the actual values themselves, which means both x and y point to the same list. So when you edit the list via the pointer either x or y, the list would update no matter refered by x or y.             
To avoid this confusion, we can state alternatively,            
```python
y = list(x)
# or
y = x[:]
```
## Elementary Operations        
To delete list elements:          
>del(x[1])           

To update the specific element:            
>areas[3] = "chill zone"             
Using the "+" to combine two vectors, but how can we construct a new vector with the elements as the addition of the corresponding elements of the two vector?           

