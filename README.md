# Manipulating-Strings-in-Python:
In this simulation project, I simulated myself working as a Security Analyst, responsible for writing Python programs to automate updating employee IDs, extracting characters from a device ID, and extracting components from a URL. I practiced creating Python code and working with strings. 

> Task 1:
*Employee IDs are currently either 4 digits or 5 digits in length. In this task, given a four-digit numeric employee ID stored in a variable called employee_id, convert this to a string format and store the result in the same variable. Later, update this employee ID string so that it complies with a new standardized format.*

code:
> Assign `employee_id` to a four digit number as an initial value
```python
employee_id = 4186

> Display the data type of `employee_id`
```python
print(type(employee_id))

> Reassign `employee_id` to the same value but in the form of a string
```python
employee_id = str(employee_id)

> Display the data type of `employee_id` now
```python
print(type(employee_id))

> output of the code:
<class 'int'>
<class 'str'>

# Task 2:
*Imagine that you have just been informed of a new criteria for employee IDs. They must all be five digits long for standardization purposes.
In this task, write a conditional statement that displays a message if the length of the employee ID is less than five digits.*

## code
> Assign `employee_id` to a four digit number as an initial value
```python
employee_id = 4186

> Reassign `employee_id` to the same value but in the form of a string

```python
employee_id = str(employee_id)

> Conditional statement that displays a message if the employee ID length is less than 5 digits
```python
if len(employee_id) < 5:
    print("This employee ID has less than five digits. It does not meet length requirements.")

> output of the code:
This employee ID has less than five digits. It does not meet length requirements.

# Task 3:
*In this task, build upon the previous code. If an employee ID is only four digits, use concatenation to create a five-digit employee ID number.
Concatenation is a process that allows you to merge strings together. The addition operator (+) in Python allows you to concatenate two strings.
Write an if statement that evaluates whether the length of employee_id is less than 5. When the condition evaluates to True, reassign employee_id by concatenating "E" in front of the four-digit employee ID to create a five character employee ID. Then, display employee_id again.*

## code:
> Assign `employee_id` to a four digit number as an initial value
```python
employee_id = 4186

> Reassign `employee_id` to the same value but in the form of a string
```python
employee_id = str(employee_id)

> Display the `employee_id` as it currently stands
```python
print(employee_id)

> Conditional statement that updates the `employee_id` if its length is less than 5 digits
```python
if len(employee_id) < 5:
    employee_id = "E" + employee_id

> Display the `employee_id` after the update
```python
print(employee_id)

> output of the code:
4186
E4186

# Task 4:
*Imagine that the characters in a device ID convey technical information about the device. Extract characters in specific positions from the device ID. Start off by extracting the fourth character. The variable device_id represents a device ID containing alphanumeric characters; it's already stored as a string.*

> Code:
> Assign `device_id` to a string that contains alphanumeric characters
```python
device_id = "r262c36"

> Extract the fourth character in `device_id` and display it
```python
print(device_id[3])

> output of the code:
2

# Task 5:
*Now extract the first through the third characters in the device ID. So take a slice of the device ID. You can achieve this using bracket notation in Python. Then, display the slice to examine the result.*

> Code:
> Assign `device_id` to a string that contains alphanumeric characters
```python
device_id = "r262c36"

> Extract the first through the third characters in `device_id` and display the result
```python
device_id[0:3]

> output:
r26

# Task 6:
*You'll work with string indices to display various components of a URL that's stored in the URL variable. First, extract and display the protocol of the URL and the :// characters that follow it using string slicing. Consider that the protocol is in the secure format of https when determining the indices for your slice.*

> Code:
> Assign `url` to a specific URL
```python
url = "https://exampleURL1.com"

> Extract the protocol of `url` along with the syntax following it, display the result
```python
print(url[0:8])

> output:
https://

# Task 7:
*Later in this project, you'll extract the domain extension. To prepare for this, use the .index() method to identify the index where the domain extension .com is located in the given URL.*

> code:
> Assign `url` to a specific URL
```python
url = "https://exampleURL1.com"

> Display the index where the domain extension ".com" is located in `url`
```python
print(url.index(".com"))

> output:
19

# Task 8:
*Store the output of the .index() method in a variable called ind, which is short for index. This index represents the position where the domain extension ".com" starts in the url. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell. Note that running this cell will not produce an output.*

> Code:
> Assign `url` to a specific URL
```python
url = "https://exampleURL1.com"

> Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url`
```python
ind = url.index(".com")

# Task 9:
*You can use string slicing to also extract the domain extension of a URL. To do so, you can create a slice. The starting index should be the ind variable. This contains the index where the domain extension begins. The ending index should be ind + 4 (since ".com" is four characters long). Sometimes, like in this situation, it's easier to express the ending index in relation to the starting index. Examine the following code, run it as is, and observe the output.*

> Code:
> Assign `url` to a specific URL
```python
url = "https://exampleURL1.com"

> Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url`
```python
ind = url.index(".com")

> Extract the domain extension in `url` and display it
```python
print(url[ind:ind+4])

> output:
.com

# Task 10:
*Finally, extract the website name from the given URL using string slicing and the ind variable that you defined earlier. In the given URL, the website name is "exampleURL1". What the length of the extracted slice?*

> Code:
> Assign `url` to a specific URL
```python
url = "https://exampleURL1.com"

> Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url`
```python
ind = url.index(".com")

> Extract the website name in `url` and display it
```python
print(url[8:ind])
> other ways of displaying this:
```python
print(url[-15:-4])
print(url[8:19])
> length of the slice:
```python
print(len(url))
> output:
exampleURL1
exampleURL1
exampleURL1
23

## Observations:
- Strings are instrumental in storing important, security-related data, such as device IDs and URLs.
- String concatenation allows you to easily combine information in a string with the information stored in another string.
- String slicing is a powerful technique that enables you to extract any subsection of a string.
- Python has many functions and methods that help analysts work with string values, as well as data that they want to convert to string format.
  - The type() function returns the data type of its input.
  - The str() function converts the input object into a string. For example, when called on an integer, str() returns that integer value converted to a string.
  - The len() function returns the number of elements in an object. When called on a string, len() returns the number of characters in that string.
  - The .index() method finds the first occurrence of the input in a string and returns its location. It provides the index where the substring begins.





























