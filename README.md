This program reads a file specified by the user and counts the number of lines it contains. It helps to quickly find out how many lines are in any text file.
```python
filename = input("Enter filename: ")

try:
    with open(filename, 'r') as file:
        lines = file.readlines()
        print(f"Number of lines: {len(lines)}")
except FileNotFoundError:
    print(f"Could not open file {filename}")
