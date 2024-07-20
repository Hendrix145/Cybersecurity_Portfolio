                          Hash Cracker Tool
An advanced tool for brute-forcing hashes using a provided wordlist.

                             FEATURES
Multiple Algorithm Support: Crack hashes made with md5, sha1, sha256, and more.
User-friendly CLI: Intuitive and easy to use.
Helpful Feedback: Receive clear and concise error messages when things go wrong.

                           Prerequisites
Python 3.x

                              Usage
Run the cracker with:
               python hash-cracker.py --hashvalue [HASH_VALUE] --hashtype [HASH_TYPE] --wordlist [PATH_TO_WORDLIST]

                           Example
To crack a MD5 hash using a wordlist:
        python /home/kali/Desktop/hash_cracker.py --hashvalue 7a10ea1b9b2872da9f375002c44ddfce --hashtype md5 --wordlist /home/kali/Desktop/python.txt
