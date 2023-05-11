# Reading and Writing Files in Python
### What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?
* ### After opening the file for reading or writing <code>with</code> statement help us to take care automatically when closing of the file. "<code>with</code> statement allows for cleaner code and makes handling any unexpected errors easier users"

### Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method.
* ### .read() : It is reading the entire file.
    example:<br></br><code>with open('dog_breeds.txt', 'r') as reader:<br></br>
            #Read & print the entire file<br></br>
            print(reader.read())<br></br>
            Pug<br></br>
            Jack Russell Terrier<br></br>
            English Springer Spaniel<br></br>
            German Shepherd<br></br>
            Staffordshire Bull Terrier<br></br>
            Cavalier King Charles Spaniel <br></br>
            Golden Retriever<br></br>
            West Highland White Terrier<br></br>
            Boxer<br></br>
            Border Terrier</code>
* ### .readline() :	This reads the remaining lines from the file object and returns them as a list.
    example:<br></br><code>f = open('dog_breeds.txt')<br></br>
        f.readlines()  # Returns a list object <br></br>
        ['Pug\n', 'Jack Russell Terrier\n', 'English Springer Spaniel\n', 'German Shepherd\n', 'Staffordshire Bull Terrier\n', 'Cavalier King Charles Spaniel\n', 'Golden Retriever\n', 'West Highland White Terrier\n', 'Boxer\n', 'Border Terrier\n']</code>

# Exceptions in Python
### Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.
* ### 