# Password_Checker

This Python script provides a simple yet effective password checking mechanism by leveraging the "Have I Been Pwned" API. The script takes a password or a list of passwords as input and checks whether they have been compromised in known data breaches.
Features:

    Hashing: Utilizes the SHA-1 hashing algorithm to securely hash passwords before sending them to the API.

    API Integration: Connects to the "Have I Been Pwned" API to retrieve information about password breaches.

    Check Frequency: Determines how many times a password has been found in known breaches, providing a measure of its security.

How it Works:

    The script hashes the password using SHA-1, converts it to uppercase, and splits it into the first five characters and the remaining tail.
    It queries the "Have I Been Pwned" API with the first five characters to retrieve a list of hashed passwords with the same prefix.
    It checks if the full hashed password (excluding the first five characters) is present in the API response, indicating a match with a breached password.
    The script then reports the number of times the password has been found or confirms that it has not been compromised.

Usage:

    Run the script from the command line, providing one or more passwords as arguments.
    Receive instant feedback on the security status of the passwords.

Example:

python password_checker.py my_secure_password

Note:

This script is a valuable tool for individuals to assess the security of their passwords and take proactive measures to enhance their online security.
