Python Data Types & Structures



    Data Type: A category for a particular type of data item that dictates how the computer will process it.

        (Context: Python automatically assigns data types when a variable is created, making it highly flexible for parsing security logs and network data.)

    String: Data consisting of an ordered sequence of characters, letters, numbers, or symbols enclosed in single or double quotation marks (e.g., "updates needed").

        (Context: Used extensively to represent and manipulate textual data like usernames, file paths, log messages, and IP addresses.)

    Integer: Numeric data consisting of a whole number without a decimal point (e.g., 500, -12, 0).

        (Context: Useful for exact mathematical operations, counting failed login attempts, or tracking the number of open network ports.)

    Float: Numeric data consisting of a number with a decimal point (e.g., 0.34, -2.2).

        (Context: Utilized when calculations require fractional representation, such as calculating threat risk scores or percentage-based compliance metrics.)

    Boolean: Data that evaluates to one of only two possible values: True or False (without quotation marks).

        (Context: Fundamental for logic gates and conditional statements, such as verifying if a user's login attempt was authorized (True) or blocked (False).)

    List: A data structure that stores a mutable (changeable), ordered sequence of elements enclosed in square brackets [] and separated by commas.

        (Context: Analysts use lists to store dynamically updating sets of data, such as compiling a running sequence of suspicious IP addresses flagged during a scan.)

    Tuple: A data structure storing an ordered collection of data that is immutable (cannot be changed), enclosed in parentheses ().

        (Context: Tuples are memory-efficient and secure; they are perfect for storing static identifiers, ensuring critical configuration data or an access control list cannot be accidentally altered by a script.)

    Dictionary: A data structure that maps data as key-value pairs, separated by colons and enclosed in curly brackets {}.

        (Context: Ideal for storing and retrieving structured data predictably, such as mapping specific User IDs (keys) to their corresponding network clearance levels (values).)

    Set: A data structure containing an unordered collection of entirely unique values, enclosed in curly brackets {}.

        (Context: Prevents duplicate entries automatically, making it highly effective for rapidly filtering out duplicate source IP addresses from massive firewall log dumps.)

Python Variables & Naming Conventions

    Variable Assignment: The process of storing data values by placing a variable name to the left of an equals sign (=) and its value to the right.

        (Context: Allows analysts to store dynamic inputs, like a user's active session state, and recall or reassign it efficiently throughout a script without hardcoding raw data.)

    Variable Syntax Rules: Python variables must only use letters, numbers, and underscores; they are strictly case-sensitive and cannot use reserved built-in keywords (e.g., if, True, print).

        (Context: Violating these strict syntax rules causes the Python interpreter to throw errors, instantly halting the execution of automated security scripts.)

    Naming Best Practices: Variables should use descriptive names, separate words with underscores, and avoid overly long or confusingly similar titles (e.g., login_attempts instead of var_3).

        (Context: Ensures that complex threat-hunting code remains cleanly documented, readable, and easily maintainable by other analysts reviewing your tools.)

Conditional Statements & Logic

    Conditional Statement: A statement that evaluates code to determine whether it meets a specific set of conditions, returning a Boolean value of True or False.

        (Context: Used to control the flow of a script, such as executing a specific block of code only if a web request returns an HTTP status code of 200.)

    Comparison Operators: Mathematical symbols used to compare values, including > (greater than), < (less than), >= (greater than or equal to), <= (less than or equal to), == (equal to), and != (not equal to).

        (Context: The == and != operators are highly utilized to verify exact string matches, such as checking if a parsed username matches a known administrator account.)

    if Statement: The foundational keyword that begins a conditional statement, requiring a condition and a colon in the header, followed by an indented body of executable code.

        (Context: Python evaluates the condition; if it evaluates to True, the indented body executes. If False, Python skips the body entirely.)

    else Statement: A keyword that specifies alternative actions to execute only when all preceding conditions in the statement evaluate to False.

        (Context: Acts as a catch-all fallback mechanism; for instance, if an IP address fails an approved list check, the else block can trigger a default block action.)

    elif Statement: Short for "else if," this keyword precedes a new condition that is evaluated sequentially only when previous conditions evaluate to False.

        (Context: Allows analysts to chain multiple specific checks together sequentially, such as routing system alerts differently based on whether a status code is 400 or 500.)

    Logical Operators (and, or, not): Keywords used to evaluate multiple conditions simultaneously or negate a condition entirely.

        (Context: and requires both conditions to be True; or requires only one to be True; not inverses the condition's Boolean value, executing code when an event falls strictly outside a specified baseline.)

Loops & Iteration

    for Loop: A control flow statement used to iterate over a specified sequence (like a list or a string) for a designated number of times.

        (Context: Extremely useful for parsing through a list of network assets, IP addresses, or usernames one by one to apply consistent security audits to each element.)

    range() Function: A built-in Python function that generates a sequence of numbers, accepting parameters for the start point (inclusive), stop point (exclusive), and increment value.

        (Context: Allows analysts to execute a block of code a specific number of times efficiently without needing to define a pre-existing list of data.)

    while Loop: A control flow statement that continues to execute an indented block of code repeatedly as long as a specified condition evaluates to True.

        (Context: Commonly used for continuous monitoring tasks or enforcing limit thresholds, such as locking an account only after a loop variable tracking failed login attempts hits a limit of 5.)

    break Keyword: A loop management command used within a conditional statement to immediately exit and terminate a for or while loop entirely.

        (Context: Optimizes script performance by stopping a system search operation the exact moment a target match is found, preventing unnecessary processing.)

    continue Keyword: A loop management command used to immediately skip the current iteration of a loop and proceed directly to the next sequence item.

        (Context: Allows security scripts to bypass irrelevant data points silently, such as skipping over offline devices in a list while continuing to port scan the remaining online targets.)

Functions & Variable Scope

    Function: A reusable section of code that can be called repeatedly throughout a program.

        (Context: Essential for maintaining clean code, allowing security analysts to package complex logic—like verifying a file hash—into a single command.)

    Built-in Functions: Functions that exist natively within Python and can be called directly without needing to be defined manually (e.g., print(), type(), max(), min(), sorted()).

        (Context: These built-in utilities speed up data parsing, allowing an analyst to instantly find the highest login duration or sort a list of IP addresses alphabetically.)

    User-Defined Functions: Custom functions that programmers design specifically for their own needs.

        (Context: Allows an analyst to tailor exact security routines, such as creating a custom function named display_investigation_message() to trigger specific alerts.)

    Function Header: The initial line of code that defines a function, starting with the def keyword, followed by the function name, parentheses (), and ending with a colon :.

        (Context: Signals to the interpreter that a new block of reusable logic is being established.)

    Function Body: An indented block of code following the function header that defines exactly what actions the function will perform when called.

        (Context: The strict indentation separates the function's internal logic from the global code outside of it.)

    Parameter: An object (variable) included inside the parentheses of a function definition header.

        (Context: Acts as a placeholder variable that waits to receive external data when the function is eventually run.)

    Argument: The actual data passed into a function's parameters when it is called (e.g., in remaining_login_attempts(3, 2), the integers 3 and 2 are arguments).

        (Context: Arguments are the live inputs—like a live username or IP address—fed into the function's static logic.)

    Return Statement: A command utilizing the return keyword to output information from a function and immediately exit the function body.

        (Context: Allows the result of a function's calculation to be stored in a variable and used elsewhere in the script, rather than just printing it to the terminal.)

    Global Variable: A variable assigned outside of a function definition that is available throughout the entire program.

        (Context: Used for universal constants, such as storing a master device_id that multiple different functions might need to read simultaneously.)

    Local Variable: A variable assigned internally within a function body, making it inaccessible to the rest of the code outside that specific function.

        (Context: Includes parameters; Python temporarily creates these in memory while the function runs and deletes them afterward, preventing variable name conflicts.)

Python Libraries & Modules

    Python Standard Library: An extensive collection of pre-built Python code and modules that comes packaged natively with Python.

        (Context: Saves security analysts from writing complex code from scratch, providing ready-to-use tools for tasks like math, file parsing, and system operations.)

    re Module: A standard module that provides functions used for searching for specific string patterns in text.

        (Context: Essential for parsing massive log files to extract specific IP addresses, email formats, or error codes using regular expressions.)

    csv Module: A standard module that provides functions used when working with comma-separated values (.csv) files.

        (Context: Allows scripts to easily read from or write to spreadsheet-like log exports from network appliances.)

    glob and os Modules: Standard modules that provide functions used when interacting directly with the operating system and command line.

        (Context: Used to automate local file management, navigate directories, and execute system-level commands during script execution.)

    time and datetime Modules: Standard modules that provide functions used when generating, parsing, and working with timestamps.

        (Context: Critical for incident response to accurately map event timelines, calculate session durations, or format log entry times.)

    statistics Module: A standard module that includes mathematical functions used for calculating statistics related to numeric data sets, such as mean() or median().

        (Context: Helpful for establishing baseline metrics, such as calculating the average number of failed login attempts to flag anomalous spikes.)

    import Keyword: A command used to search for a full module or library in a system and add it to the local Python environment.

        (Context: When importing an entire module (e.g., import statistics), you must prefix its functions with the module name and a period when calling them (e.g., statistics.mean()).)

    from Keyword: A command used alongside import to extract only specific, targeted functions from a module rather than the entire library.

        (Context: Using from statistics import mean allows you to call the function directly as mean() without the module prefix, keeping script syntax cleaner.)

    External Libraries: Third-party collections of code, such as Beautiful Soup (bs4) for HTML parsing or NumPy (numpy) for arrays, that are not included in the standard library.

        (Context: Must be downloaded and installed into the environment before they can be imported and utilized in a script.)

    %pip install: The package management command used within a notebook environment to download and install external Python libraries.

        (Context: Executing %pip install numpy fetches the library from the Python Package Index, making it available for the import numpy command.)
