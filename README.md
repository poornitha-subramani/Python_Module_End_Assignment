# 🎫 Customer Support Ticket Analyser

A Python-based Customer Support Ticket Analysis System that stores, cleans, processes, and analyses customer support tickets.

## 📌 Project Overview

Customer support teams handle numerous service tickets every day. Analysing support tickets helps identify common issues, understand customer concerns, analyse ticket priorities, and extract useful insights.

In this project, a Python-based Ticket Analysis System is developed to:

- Store customer support tickets
- Add new tickets dynamically
- Validate ticket priorities
- Clean issue descriptions
- Analyse keywords
- Analyse ticket priorities
- Find the longest issue description
- Extract unique words
- Display final cleaned ticket data


## 🎯 Problem Statement

The objective of this project is to build a Python-based Customer Support Ticket Analyser that stores, cleans, analyses, and extracts useful information from customer support tickets.

The project uses Python data structures and programming concepts to process customer support information.


# 🔹 STEP 1: PRELOADED TICKETS

The program begins with a dictionary containing 10 preloaded customer support tickets.

Each ticket contains:

- Ticket Number
- Customer Name
- Issue Description
- Priority

### Initial Ticket Numbers

The initial tickets are numbered:

1, 2, 3, 4, 5, 6, 7, 8, 9, 10

### Customer Names

The preloaded customers are:

- Ravi
- Meera
- Sam
- Anu
- Rakesh
- Divya
- Arjun
- Kiran
- Leela
- Nisha

### Ticket Fields

The ticket dictionary contains:

- `Ticket_No`
- `Customer_Name`
- `Issue_Description`
- `Priority`

### Display Initial Ticket Data

A function named `show_data()` is used to display the initial ticket data in a readable format.


# 🔹 STEP 2: ADD MORE TICKETS

The program asks the user:

    How many new tickets do you want to add?

For every new ticket, the program collects:

- Customer Name
- Issue Description
- Priority

### Automatic Ticket Number

The ticket numbers are automatically generated.

The initial tickets end at Ticket 10, so new tickets start from Ticket 11.

For example:

    Ticket 11
    Ticket 12
    Ticket 13

and so on.

### Priority Validation

The program accepts only the following priority values:

- High
- Medium
- Low

If an invalid priority is entered, the program displays an error message and asks the user to enter a valid priority.

### Example

    How many new tickets do you want to add? 2

    Customer Name: Priya
    Issue Description: Internet is very slow
    Priority (High/Medium/Low): High

    Ticket 11 added.

The new ticket information is appended to the existing `ticket_data`.



# 🔹 STEP 3: TEXT CLEANING FOR ISSUE DESCRIPTIONS

All issue descriptions are cleaned before performing analysis.

The text-cleaning process includes:

### 1. Convert Text to Lowercase

Example:

    GREAT SUPPORT!

becomes:

    great support

### 2. Remove Punctuation

The program removes punctuation such as:

    .
    ,
    !
    ?
    -

Example:

    Internet not working!!!

becomes:

    internet not working

### 3. Remove Extra Spaces

Multiple spaces are converted into a single space.

Example:

    poor    handling    of    issue

becomes:

    poor handling of issue

### 4. Remove Leading and Trailing Spaces

Example:

    "   Internet not working   "

becomes:

    "internet not working"

### 5. Replace Slang and Short Forms

Common slang and shorthand words are replaced with standard words.

| Short Form | Replacement |
|------------|-------------|
| ok | okay |
| pls | please |
| plz | please |
| thx | thanks |
| u | you |
| ur | your |
| gr8 | great |
| bcoz | because |
| b4 | before |
| asap | as soon as possible |

### Text Cleaning Function

The project uses a function named:

    clean_text(text)

This function performs the required text-cleaning operations.

The cleaned descriptions are stored back into:

    ticket_data['Issue_Description']


# 🔹 STEP 4: KEYWORD-BASED ISSUE INSIGHTS

The project performs keyword-based analysis on the cleaned issue descriptions.

A function named:

    count_tickets_with_word(word)

is created to count how many ticket descriptions contain a specified word.

### Function Requirements

The function performs a case-insensitive search.

For example:

    GOOD
    Good
    good

are treated as the same keyword.

### Keywords Analysed

The program analyses these four keywords:

- poor
- good
- slow
- excellent

### Example Output

    === KEYWORD INSIGHTS ===

    Number of tickets containing "poor": ...
    Number of tickets containing "good": ...
    Number of tickets containing "slow": ...
    Number of tickets containing "excellent": ...

This analysis helps identify commonly occurring words in customer support issue descriptions.


# 🔹 STEP 5: FINAL SUMMARY & INSIGHTS

After adding and cleaning the tickets, the program produces the final analysis.

The final analysis contains four main sections.

---

## 5.1 DISPLAY FINAL CLEANED TICKET DATA

The program displays the complete ticket data after cleaning the issue descriptions.

The final data contains:

- Ticket Number
- Customer Name
- Cleaned Issue Description
- Priority

The `show_data()` function is used to display the final cleaned ticket data.

---

## 5.2 PRIORITY ANALYSIS

The program calculates the number of tickets in each priority category.

The categories are:

- High
- Medium
- Low

### Output

    === PRIORITY ANALYSIS ===

    Number of High-priority tickets: ...
    Number of Medium-priority tickets: ...
    Number of Low-priority tickets: ...

This provides an overview of the distribution of support tickets according to priority.


## 5.3 FIND THE TICKET WITH THE LONGEST ISSUE DESCRIPTION

The program calculates the word count of every cleaned issue description.

The ticket with the highest word count is identified.

The following information is displayed:

- Ticket Number
- Customer Name
- Cleaned Issue Text
- Word Count

### Output

    === LONGEST ISSUE DESCRIPTION ===

    Ticket number : ...
    Customer name : ...
    Cleaned issue : ...
    Word count    : ...

If more than one ticket has the same maximum word count, all matching tickets are displayed.

---

## 5.4 EXTRACT UNIQUE WORDS USED

The program creates a set containing all unique words from all issue descriptions.

A Python set is used because it automatically removes duplicate words.

The program displays:

- Count of unique words
- Sorted list of unique words

### Output

    === UNIQUE WORDS ===

    Count of unique words: ...
    Word list (sorted): [...]

The unique words are sorted alphabetically before being displayed.


# 🧠 PYTHON CONCEPTS USED

This project demonstrates the following Python concepts:

- Dictionaries
- Lists
- Sets
- Functions
- For loops
- While loops
- Conditional statements
- Exception handling
- User input
- Input validation
- String manipulation
- List comprehension
- Set operations

### Important String Methods Used

    .lower()
    .strip()
    .split()
    .replace()
    .join()

### Functions Used

    show_data(data)

    clean_text(text)

    count_tickets_with_word(word)



# 🔄 PROJECT WORKFLOW

The complete project workflow is:

    Step 1
    ↓
    Load 10 Preloaded Tickets
    ↓
    Display Initial Ticket Data
    ↓
    Step 2
    ↓
    Add New Tickets
    ↓
    Validate Priority
    ↓
    Append New Ticket Data
    ↓
    Step 3
    ↓
    Clean Issue Descriptions
    ↓
    Convert to Lowercase
    ↓
    Remove Punctuation
    ↓
    Remove Extra Spaces
    ↓
    Replace Slang
    ↓
    Step 4
    ↓
    Perform Keyword Analysis
    ↓
    Analyse poor / good / slow / excellent
    ↓
    Step 5
    ↓
    Display Final Cleaned Data
    ↓
    Perform Priority Analysis
    ↓
    Find Longest Issue Description
    ↓
    Extract Unique Words
    ↓
    Display Final Insights


# ✨ KEY FEATURES

- ✅ 10 preloaded customer support tickets
- ✅ Dynamic ticket creation
- ✅ Automatic ticket numbering
- ✅ Ticket numbering starts from 11 for new tickets
- ✅ Customer name input
- ✅ Issue description input
- ✅ Priority validation
- ✅ High / Medium / Low priority classification
- ✅ Text cleaning
- ✅ Lowercase conversion
- ✅ Punctuation removal
- ✅ Extra-space removal
- ✅ Leading and trailing space removal
- ✅ Slang and shorthand replacement
- ✅ Case-insensitive keyword search
- ✅ Keyword-based issue analysis
- ✅ Priority analysis
- ✅ Longest issue description detection
- ✅ Word count calculation
- ✅ Unique word extraction
- ✅ Sorted unique-word list
- ✅ Final cleaned ticket dataset


# 📊 EXPECTED OUTPUT SECTIONS

The program produces the following major output sections:

    === INITIAL TICKET DATA ===

    === KEYWORD INSIGHTS ===

    === FINAL CLEANED TICKET DATA ===

    === PRIORITY ANALYSIS ===

    === LONGEST ISSUE DESCRIPTION ===

    === UNIQUE WORDS ===


# 💻 SAMPLE USER INTERACTION

    How many new tickets do you want to add? 1

    Customer Name: Priya

    Issue Description: Internet is very slow!!!

    Priority (High/Medium/Low): High

    Ticket 11 added.

The program then cleans the new issue description and includes it in the final analysis.


# 📈 SAMPLE ANALYSIS OUTPUT

    === KEYWORD INSIGHTS ===

    Number of tickets containing "poor": ...
    Number of tickets containing "good": ...
    Number of tickets containing "slow": ...
    Number of tickets containing "excellent": ...


    === PRIORITY ANALYSIS ===

    Number of High-priority tickets: ...
    Number of Medium-priority tickets: ...
    Number of Low-priority tickets: ...


    === LONGEST ISSUE DESCRIPTION ===

    Ticket number : ...
    Customer name : ...
    Cleaned issue : ...
    Word count    : ...


    === UNIQUE WORDS ===

    Count of unique words: ...
    Word list (sorted): [...]



# 📂 PROJECT STRUCTURE

    Customer-Support-Ticket-Analyser/
    │
    ├── customer_support_ticket_analyser.py
    │
    └── README.md

# 📚 LEARNING OUTCOMES

Through this project, I strengthened my understanding of:

- Python programming fundamentals
- Dictionaries
- Lists
- Sets
- Functions
- Loops
- Conditional statements
- Exception handling
- User input validation
- String manipulation
- Text preprocessing
- Keyword searching
- Basic data analysis
- Data cleaning
- Problem-solving
- Writing structured Python programs

This project helped me understand how Python programming concepts can be combined to solve a simple real-world data analysis problem.

# 🚀 FUTURE ENHANCEMENTS

The project can be further enhanced by adding:

- 📊 Data visualisation
- 📈 Ticket trend analysis
- 📁 CSV file support
- 📊 Excel file support
- 🗄️ Database integration
- 😊 Sentiment analysis
- 🔎 Advanced text search
- 🖥️ Graphical User Interface
- 📊 Interactive dashboard
- 🤖 Machine learning-based ticket classification
- 📌 Ticket status tracking
- 📅 Ticket date and time tracking
- 📧 Automated customer support notifications


