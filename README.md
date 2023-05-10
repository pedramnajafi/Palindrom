# Palindrom
A palindrome is a word, number, phrase, or other sequence of symbols that reads the same backwards as forwards, such as the words madam or racecar, the date and time 11/11/11 11:11, and the sentence: "A man, a plan, a canal – Panama".

    run = True
    while run:
        user_input = input('Please type a word or number to check if it is a Palindrom or not or type exit: ')
        if user_input == 'exit':
            run = False
            break
        user = ''.join(filter(str.isalnum, user_input)) # removes all the non-alphanumic characters.
        lowercase = user.lower() # turn the input word into a lowercase word - dows nothing on numbers.
        characters = list(lowercase) # turn the input word into a list of characters.
        length = len(characters) # counts the number of characters
        for c,i in zip(characters, range(length)):
            reverse_char = characters[(length - 1 - i)]
            if c != reverse_char:
                print(False)
                break
            else :
                if i == length-1:
                    print(True)



