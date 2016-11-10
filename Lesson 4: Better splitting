# The built-in <string>.split() procedure works
# okay, but fails to find all the words on a page
# because it only uses whitespace to split the
# string. To do better, we should also use punctuation
# marks to split the page into words.

# Define a procedure, split_string, that takes two
# inputs: the string to split and a string containing
# all of the characters considered separators. The
# procedure should return a list of strings that break
# the source string up by the characters in the
# splitlist.

#My code is different from the answer.
#The answer has a True/False switch, nice design!

#This is my code:
def split_string(source,splitlist):
    output = []
    start = 0
    end = 0
    while end < len(source):
        if source[start] not in splitlist:
            if source[end] in splitlist:
                output.append(source[start:end])
                start = end + 1
            elif end == len(source) - 1:
                output.append(source[start:])
        else:
            start = start + 1
        end = end + 1
    return output
    
#This is the answer code:
def split_string(source,splitlist):
    output = []
    atsplit = True
    for char in source:
        if char in splitlist:
            atsplit = True
        else:
            if atsplit:
                output.append(char)
                atsplit = False
            else:
                output[-1] = output[-1] + char
