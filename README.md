# Module 2: Hash Table Implementation using Python Dictionaries

## Description
This project implements a contact agenda using Python's native `dict` data structure to demonstrate the efficiency of Hash Tables over linear and binary searches.

## Features (CRUD)
- **Create (`add_contact`)**: Inserts a new contact. Validates existence with `in` to prevent accidental overwrites.
- **Read (`search_contact`)**: Retrieves phone numbers using `.get()`, validating against `None` to handle empty strings or falsy values correctly.
- **Update (`update_contact`)**: Modifies an existing contact's phone number.
- **Delete (`delete_contact`)**: Removes a contact using the `del` keyword.

## Theoretical Justification: The 'Zulema' Case Study

### Scenario
An agenda containing **100 contacts ordered alphabetically**, searching for **"Zulema"** (located near or at the end of the list).

1. **Binary Search ($O(\log n)$)**:
   - On an ordered list of $N = 100$ items, binary search recursively divides the search space in half.
   - Total operations: $\lceil \log_2(100) \rceil \approx 7$ comparison steps to locate "Zulema".

2. **Dictionary / Hash Table ($O(1)$)**:
   - The dictionary computes the hash value directly from the key `"Zulema"`.
   - Access time is constant ($O(1)$), completing the search in **1 single step** regardless of alphabetical order or size ($N$).

## Running Tests
To run the automated tests suite, execute:
`pytest modulo2_hashing/test_agenda.py`
