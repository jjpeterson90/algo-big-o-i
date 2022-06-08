# Big O Answers

## Snippet 1 -
### Big O: O(N)
### Explanation: As array grows in size, the time it takes grows linearly.
```python
def largest(array, value):
  for item in array:
    if item > value:
      return False
  return True 
```


## Snippet 2 -
### Big O: O(2N) == O(N)
### Explanation: Loops once through the same dataset two separate times.

```python
def info_dump(customers):
  
  print('Customer Names:')
  for customer in customers: 
    print(customer['name'])
  
  print('Customer Locations:')
  for customer in customers: 
    print(customer['country'])
  
```

## Snippet 3 -
### Big O: O(1)
### Explanation: Only one action is performed regardless of dataset size

```python
def first_element_is_red(array):
  return array[0] == 'red' 
```

## Snippet 4 -
### Big O: O(N^2)
### Explanation: O(N) loop with an O(N) loop inside of it. O(N) is performed N times. N * N = N^2

```python
def duplicates(array):
  for index1, item1 in enumerate(array):
    for index2, item2 in enumerate(array):
      if index1 == index2:
        continue
      if item1 == item2:
        return True
  return False
``` 

## Snippet 5 -
### Big O: O(N * M) roughly equal to O(N^2). Best case is O(N), if either array remains constant size.
### Explanation: O(N) inside an O(N). Time complexity is slightly offset from N^2 since both datasets can have different sizes, but can be considered O(N^2) in worst case scenario

```python
words = ['chocolate', 'coconut', 'rainbow']
endings = ['cookie', 'pie', 'waffle']

for word in words:
  for ending in endings:
    print(word + ending)

```

## Snippet 6 -
### Big O: O(10N) = O(N)
### Explanation: One iteration over a loop of size (N). O(10) if size remains static, O(N) if size can grow.

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

def print_array(array):
  for item in array:
    print(item)

```

## Snippet 7 -
### Big O:  O(N^2)
### Explanation:  O(N) loop with a growing zero-to-N loop inside. Can be simplified to N^2.

```python
# this is insertion sort
def insertionSort(arr): 
  for i in range(1, len(arr)): 
    key = arr[i] 
    j = i-1
    while j >=0 and key < arr[j] : 
      arr[j+1] = arr[j] 
      j -= 1
    arr[j+1] = key 
```

## Snippet 8 -
### Big O:  O(N^2)
### Explanation:  O(N) loop with a decaying N-to-zero loop inside. Can be simplified to N^2.

```python
for i in range(len(my_list)):
  min_idx = i
  for j in range(i+1, len(my_list)):
      if my_list[min_idx] > my_list[j]:
          min_idx = j

  my_list[i], my_list[min_idx] = my_list[min_idx], my_list[i]
```
