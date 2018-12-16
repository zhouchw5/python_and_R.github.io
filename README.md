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

