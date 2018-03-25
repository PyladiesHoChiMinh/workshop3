### Introducing and wWorking with lists
---
Hello and welcome back the third workshop of Pyladies - Ho Chi Minh chapter,

This time we will continue to learn about an introduction of `list` and work on some simple examples of this data structure.

For some of you who have not followed us since the first workshop begun, please checkout the last session for more references.

* Workshop1: Get started with `Jupyterlab` and `git`
* Workshop2: Variable with `str` and numbers. How to write a good script with `PEP8`

Again, the main content of this workshop is mostly adapted from "Python Crash Course: A Hands-on, Project-based Introduction to Programming" by Eric Matthews and "Developer Class" by Google in `python 3`.

Alright, let us get started!

### Outline
0. What is a list? How to access elements in a list
1. Modifying, adding, inserting/ removing elements
3. Loop through an entire list with some notices
4. Make numerical lists with some statistics
5. Simple statistics with a list of numbers
6. Define a tuple and looping through all values in a tuples


#### 0. What is a list?
In simple words, `list` is a collection of many items in a order. Every elements can be `str`, `int`, `float`, and event `list` itself. Open an your `Jupyterlab` and let us know how your list variable looks like.
```python
"""
Example of a list
"""
vietnam_cities = ["Hanoi", "Hai Phong", "Hue", "Danang", "Saigon"]
print(vietnam_cities)
```
To get an access to an element or a sub-list from an original list, we use `index`, or a position of a list. *Note* Different from other programming language, an `index` of a `list` starts with 0.

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
#### 1. Modifying, adding, inserting/ removing elements

In this section, we will try to show you how to manipulate with elements in python with simple and easy examples. To begin, let us start with a story.

[a picture here]

Summer is coming. Imagine that we are planning for a vacation. Let us say `my_cities` is a list of cities in a list of `vietnam_cities` you would like to travel in an upcoming trip.

First of all, let us create a copy of a list

```python
my_cities = vietnam_cities[:]    #Get a copy of vietnam_cities
print(my_cities)
```
**Remember**: Use `[:]` at the end of a variable you want to copy unless any change you update to either `vietnam_cities` or `my_cities` will affect on another.

However, there are some missing, and some are not belong to your favorite one. Suppose "Vinh" is a city you would like to visit instead of "Hue". How would you do to update `my_cities`?

There are many ways to do. Let us try with some most basic manipulation.
##### Modifying
If we want to visit "Vinh" after "Hanoi" ...
```python
vietnam_cities[1] = "Vinh"
print(vietnam_cities)
```

##### Adding
If we want to visit "Vinh" after arriving "Saigon" (in case still have money and time)
```python
vietnam_cities.append("Vinh")
print(vietnam_cities)
```

##### Inserting/ Removing
If we want to visit "Vinh" first ...

```python
vietnam_cities.insert(0,"Vinh")
print(vietnam_cities)
```

What if "Vinh" is the last ...
```python
vietnam_cities.insert(-1,"Vinh")
print(vietnam_cities)
```

Ok, we have done a lot planning, there are something wrong, what should we do?
```python
del vietnam_cities[0]
del vietnam_cities[-1]
print(vietnam_cities)
```

Well, if we would not like to visit "Vinh" anymore ...
```python
vietnam_cities.remove("Vinh")
print(vietnam_cities)
```

#### 5. Simple statistics with a list of numbers
```python
visit_days = [1,2,3,4,5]
min(visit_days)
max(visit_days)
sum(visit_days)
```

```python
triples = [value ** 3 for values in visit_days]
print(triples)
```

#### 6. Define a tuple and looping through all values in a tuple

`Tuple` is an immutable `list`, which means that you can not change an oder or make any modification. To understand, let us come up with some examples

##### How to initialize a tuple
```python
carried_items = ("t-shirt", "shoes", "pairs of pants", "sunglasses")
print(carried_items[0])
print(carried_items[-1])
```
Try to update a tuple?
```python
carried_items[1] = "sandals"
```
No, it won't work. The only way is that we set up a new value of that tuple.

```python
carried_items = ("t-shirt", "shoes", "pairs of pants", "sunglasses")
for item in carried_items:
  print(item)

carried_items = ("t-shirt", "sandals", "pairs of pants", "sunglasses")
for item in carried_items:
  print(item)
```
### Review

To end this lesson, here are some of methods used for `list` (Adapted from `Google Developer Class in Python`)
* `list.append(elem)` -- adds a single element to the end of the list. Common error: does not return the new list, just modifies the original.
* `list.insert(index, elem)` -- inserts the element at the given index, shifting elements to the right.
* `list.extend(list2)` adds the elements in list2 to the end of the list. Using + or += on a list is similar to using `extend()`.
* `list.index(elem)` -- searches for the given element from the start of the list and returns its index. Throws a `ValueError` if the element does not appear (use "in" to check without a ValueError).
* `list.remove(elem)` -- searches for the first instance of the given element and removes it (throws ValueError if not present)
* `list.sort()` -- sorts the list in place (does not return it). (The sorted() function shown below is preferred.)
* `list.reverse()` -- reverses the list in place (does not return it)
* `list.pop(index)` -- removes and returns the element at the given index. Returns the rightmost element if index is omitted (roughly the opposite of append()).
