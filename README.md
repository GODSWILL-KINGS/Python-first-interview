# Python-first-interview

from pprint import pprint
# To  find the most repeated character in a text
sentence = "The man is destined for success"

# lets start by defining an empty dictionary

char_frequency = {}
for char in sentence:
    if char in char_frequency:
        char_frequency[char] += 1
    else:
        char_frequency[char] = 1
# print(char_frequency)
# this is quite not readable
# lets import pprint module

# pprint(char_frequency, width=1)

# using pprint was fine but char was not sorted

char_frequency_sorted=sorted(char_frequency.items(), 
key=lambda kv: kv[1], reverse=True)
print(char_frequency_sorted[0])
