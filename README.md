# PY_OLA-4_Acorda_Iteration

def main():
    word_bank = []
    
    print("Fredrickson C. Acorda | 2BSIT-1")
    print("-------------------------------")
    while True:
        word = input("\nEnter a word: ")
        while word.isdigit():
            print("Wrong input. Please enter a word.")
            word = input("Enter a word: ")
        word_bank.append(word)
        print("You entered the word", word + ".")

        choice = input("Do you want to try again? [Y/N] ").upper()
        if choice != 'Y':
            break

    num_words = len(word_bank)
    if num_words == 1:
        print("You entered 1 word:")
    else:
        print("You entered", num_words, "words:")

    print("\nThe words you entered are:")
    print("------------------------")
    for word in word_bank:
        print("| {:<20} |".format(word))
    print("------------------------")

if __name__ == "__main__":
    main()
