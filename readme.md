from pprint import pprint
<!-- To find the most repeated character in the text -->
sentence = "This is the best way to start"

char_frequency = {}
for char in sentence:
    if char in char_frequency:
        char_frequency[char] +=1
    else:
        char_frequency[char] = 1
print(char_frequency)

<!-- but this output is not readable, lets import a module pprint -->

pprint(char_frequency, width=1)
<!-- this is better -->

<!-- but lets sort it -->

char_frequency_sorted = sorted(char_frequency.items(), key=lambda kv: kv[1], reverse= True)

print(char_frequency_sorted[0])

