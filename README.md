<h2>Automate Cybersecurity Tasks With Python</h2>

In my comprehensive training, I gained proficiency in Python programming, emphasizing its applications in cybersecurity. I delved into foundational concepts like data types, variables, and control structures, aligning them with cybersecurity contexts. I broadened my skills by exploring pre-built and user-defined functions and harnessing the power of modules for reusable code. Readability became a priority, so I employed pre-built functions, crafted my functions, and practiced module utilization to improve code clarity.

My Python journey extended to string and list manipulation, with a focus on methods applicable to these data types. I utilized this knowledge to create algorithms and employ regular expressions for string pattern recognition. The application of Python to automate cybersecurity tasks, particularly those involving file operations, marked a significant milestone. I adeptly opened, read, and parsed files, culminating in structured content. The training concluded with strategies for effective code debugging, rounding out my practical Python capabilities. This extensive training equips me with a multifaceted skill set to automate tasks, manage files, and develop efficient and readable code in cybersecurity contexts.

Project Activity: Updating a file through a Python algorithm

<h4>Project Description:</h4> 

In my organisation, we regulate access to restricted content by implementing an allow list of IP addresses. The IP addresses are identified in the `"allow_list.txt"` file. A distinct list is used to identify IP addresses that should no longer be granted access to this content. I have developed an algorithm that automates the process of updating the `"allow_list.txt"` file by removing any IP addresses that should no longer have access. 

Open the file that contains the allow list

To begin the algorithm, I opened the file named `"allow_list.txt"`. First, I assigned the file name as a string to the variable `import_file`:

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/ce4f656a-0787-47a4-aa79-ea6def27f777)

Then, I used a with statement to open the file:

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/7d1efd48-ac60-48c9-a925-e979783adeaf)

The algorithm utilises the `with` statement in conjunction with the `.open()` function in read mode to open the allow list file for the explicit purpose of reading its contents. The objective of accessing the file is to enable the retrieval of the IP addresses stored within the allow list file. The utilisation of the `"with"` keyword facilitates resource management by automatically closing the file upon exiting the `"with"` statement. In the code snippet `with open(import_file, "r") as file:`, the `open()` function is utilised with two parameters. The initial step involves specifying the file to be imported, followed by indicating the desired action to be performed on the file. In this particular scenario, the letter `"r"` denotes my intention to engage in the act of reading. The code also utilises the `"as"` keyword to assign a variable named `"file"`. This variable is used to store the output of the `".open()"` function while operating within the `"with"` statement.

Read the file comment

To access the contents of the file, the `.read()` method was utilised to convert it into a string format.

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/c0af937b-9ff1-4610-9e31-6a1a9e01ebfa)

When utilising the `.open()` function with the `"r"` argument, which stands for `"read,"` it is possible to invoke the `.read()` function within the body of the with statement. The `".read()"` method facilitates the conversion of the file into a string and enables the user to access its contents for reading purposes. I utilised the `.read()` method on the `file` variable specified within the with statement. Next, I assigned the string output of this method to the variable `"ip_addresses` 

To summarise, this code retrieves the contents of the `"allow_list.txt"` file and stores them as a string. This string can be utilised in my Python programme for data organisation and extraction purposes.

Convert the string to a list

To effectively exclude individual IP addresses from the allow list, it was necessary to convert it into a list format. Subsequently, I employed the `.split()` method to transform the `ip_addresses` string into a list.

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/74afbb0e-eea5-423e-a68b-728d16b8a91a)

The `.split()` function is invoked by appending it to a string variable. The functionality involves the conversion of the string's contents into a list. The objective of dividing `ip_addresses` into a list is to facilitate the process of removing IP addresses from the allow list. The default behaviour of the `.split()` function is to divide the text into list elements based on whitespace. The algorithm utilises the `.split()` function to convert the data stored in the variable `ip_addresses`. This variable contains a string of IP addresses, each separated by a whitespace. The `.split()` function transforms this string into a list of IP addresses. In order to store this list, I have reassigned it to the variable `"ip_addresses"`. 

Itereate through the remove list 

One crucial aspect of my algorithm entails the process of iterating through the IP addresses that are elements within the `remove_list`. In order to accomplish this task, I have implemented a `for` loop.

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/74781f52-7300-4473-a048-65bc36e57d12)

The `for` loop in Python iterates over a specified sequence, allowing code to be repeated. The primary objective of the `for` loop in a Python algorithm such as this is to execute specific code statements for each element within a sequence. The `"for"` keyword is used to initiate the execution of a `for` loop. The loop variable element is subsequently followed by the keyword `"in"`. The keyword `"in"` is used to iterate through the sequence `"ip_addresses"` and assign each value to the loop variable `"element"`. 

Remove IP addresses that are on the remove list

The algorithm necessitates the removal of any IP address from the allow list, `ip_addresses`, that is also present in the `remove_list`.  As there were no duplicate entries in the `ip_addresses`, I utilised the following code to accomplish this task:

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/ef226ad8-c528-4916-b998-e941d4782d13)

Within the for loop, a conditional was implemented to evaluate the presence of the loop variable `"element"` in the `"ip_addresses"` list. I performed this action to prevent any potential errors that may occur when applying the `.remove()` method to elements that are not present in the `ip_addresses` collection. 

Subsequently, I utilised the `.remove()` method on the `ip_addresses` within the specified conditional. I utilised the loop variable element as the argument in order to remove each IP address present in the `remove_list` from the `ip_addresses`.

Update the file with the revised list of IP addresses

As the concluding phase of my algorithm, it was necessary to modify the allow list file by incorporating the updated roster of IP addresses. In order to accomplish this, it was necessary to convert the list back into a string. I utilised the `.join()` method to accomplish this task:

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/73b7716e-777b-407c-a4f5-e8fb100c23ec)

The `.join()` method is utilised to concatenate all elements within an iterable into a single string. The `.join()` method is utilised on a string that includes characters to serve as separators between the elements in the iterable when they are combined into a single string. In this algorithm, the `.join()` method was utilised to generate a string from the list `ip_addresses`. This string was subsequently passed as an argument to the `.write()` method for writing to the file `"allow_list.txt"`. I utilised the string `("n")` as the designated separator in Python to ensure that each element is placed on a separate line. 

Next, I utilised another `'with'` statement along with the `'.write()'` method to perform the file update.

![image](https://github.com/clintonsenaye/ClintonSenaye/assets/57267374/cf7ab959-e652-4ba8-a663-2ba0ea8d877b)

For this instance, I utilised a supplementary argument of `"w"` when employing the `open()` function within my with statement. This statement suggests that there is a desire to access a file in order to overwrite its existing contents. When utilising the argument `"w"`, it is possible to invoke the `.write()` function within the body of the with statement. The `.write()` function is used to write string data to a designated file, effectively replacing any pre-existing content within the file. 

In this scenario, the objective is to write the updated allow list as a string to the file named `"allow_list.txt"`. By implementing this approach, the restricted content will effectively become inaccessible to any IP addresses that have been removed from the allow list. In order to modify the file, I utilised the`.write()` function and applied it to the file object named `"file"` that was previously identified within the with statement. I provided the `ip_addresses` variable as an argument to indicate that the data within the file specified in the with statement should be overwritten with the contents of this variable.

Summary 

I have developed an algorithm that effectively eliminates IP addresses, as specified in the `remove_list` variable, from the `"allow_list.txt"` file containing the list of authorised IP addresses. The algorithm entails the following steps: firstly, opening the file; secondly, converting the file into a string format for reading purposes; and finally, converting this string into a list, which will be stored in the variable `"ip_addresses"`. I proceeded to iterate through the IP addresses in the `remove_list`. During each iteration, I assessed whether the element was included in the `ip_addresses` list. I utilised the `.remove()` method to eliminate the element from the `ip_addresses`. Subsequently, the `.join()` method was utilised to convert the `ip_addresses` into a string format, facilitating the overwriting of the `"allow_list.txt"` file with the updated list of IP addresses.
