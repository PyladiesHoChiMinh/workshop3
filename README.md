#### Introducing lists + Working with lists

Hello and welcome back the third workshop of `Pyladies`,

This time we will continue to learn about an introduction of `list` and work on some simple examples of this data structure. For those of you who have not followed us since the first workshop begun, please checkout the last session for some references. Also, the main content of this workshop is mostly adapted from "Python Crash Course: A Hands-on, Project-based Introduction to Programming" by Eric Matthews and "Developer Class" by Google in python 3.

Alright, let us get started!

#### Outline
0. What is a list? How to access elements in a list
1. Modifying, adding, inserting/ removing elements
3. Loop through an entire list with some notices
4. Make numerical lists with some statistics
5. Simple statistics with a list of numbers
6. Define a tuplea and looping through all values in a tuples


##### 0. What is a list?

```python
"""
Example of a list
"""
vietnam_cities = ["Hanoi", "Hai Phong", "Hue", "Danang", "Saigon"]
print(vietnam_cities)
```

We could say `list` is a collection of many items in a order. Each of them can be `str`, `int`, `float`.  Open an your `Jupyterlab` and let us know how your list variable looks like. To get an access to an element or a sub-list from an original list, we use `index`, or a position of a list. *Note* Different from other programming language, an `index` of a `list` starts with 0.

Try the following print function and let us know how it works.

```python
"""
Example of accessing a list
"""
print(vietnam_cities[0])    # The fist element
print(vietnam_cities[-1])   # The last element
print(vietnam_cities[::-1])   # Reverse an order
print(vietnam_cities[:-1:])   # Start from the second element from the last
```
##### 1. Modifying, adding, inserting/ removing elements

In this session, we will try to show you how to manipulate with elements in python with simple and easy examples.

Imagine that we would like to add another city into `vietnam_cities`, for example, "Vinh".

###### Modifying

```python
vietnam_cities[1] = "Vinh"
print(vietnam_cities)
```

###### Adding

```python
vietnam_cities.append("Vinh")
print(vietnam_cities)
```

###### Inserting/ Removing

```python
vietnam_cities.insert(0,"Vinh")
print(vietnam_cities)
```
```python
vietnam_cities.insert(-1,"Vinh")
print(vietnam_cities)
```

```python
del vietnam_cities[0]
del vietnam_cities[-1]
print(vietnam_cities)
```
```python
vietnam_cities.remove("Vinh")
print(vietnam_cities)
```

##### 5. Simple statistics with a list of numbers
##### 6. Define a tuplea and looping through all values in a tuples

More reading:
- Workshop1: Get started with `Jupyterlab` and `git`
- Workshop2: Learn about variable and how to write a good work.
