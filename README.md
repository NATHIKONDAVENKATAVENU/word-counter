def get_user_input():
    """
    Prompt the user to enter a sentence or paragraph.
    """
    text = input("Enter a sentence or paragraph: ")
    return text

def count_words(text):
    """
    Count the number of words in the input text.
    """
    words = text.split()
    return len(words)

def print_word_count(word_count):
    """
    Print the word count to the console.
    """
    print("Word count:", word_count)

def handle_empty_input(text):
    """
    Handle empty input by prompting the user until a non-empty input is provided.
    """
    while not text.strip():
        print("Error: Input cannot be empty.")
        text = input("Please enter a sentence or paragraph: ")
    return text

def main():
    # Get user input
    text = get_user_input()

    # Handle empty input
    text = handle_empty_input(text)

    # Count words
    word_count = count_words(text)

    # Print word count
    print_word_count(word_count)

if __name__ == "__main__":
    main()
          
