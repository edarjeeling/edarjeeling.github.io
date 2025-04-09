class Tokenizer:
    def __init__(self):
        # Dictionary to store word frequencies
        self.word_freq = {}
        # List to store all tokens
        self.tokens = []
        
    def tokenize(self, text):
        """
        Convert text into tokens (words)
        """
        # Convert to lowercase
        text = text.lower()
        
        # Replace common punctuation with spaces
        punctuation = '''!()-[]{};:'"\,<>./?@#$%^&*_~'''
        for char in punctuation:
            text = text.replace(char, ' ')
            
        # Split into words and remove empty strings
        self.tokens = [word.strip() for word in text.split() if word.strip()]
        
        # Update word frequency dictionary
        self.word_freq.clear()
        for token in self.tokens:
            self.word_freq[token] = self.word_freq.get(token, 0) + 1
            
        return self.tokens
    
    def get_tokens(self):
        """
        Return the list of tokens
        """
        return self.tokens
    
    def get_vocabulary(self):
        """
        Return unique words
        """
        return list(self.word_freq.keys())
    
    def get_word_frequency(self):
        """
        Return dictionary of word frequencies
        """
        return self.word_freq
    
    def get_token_count(self):
        """
        Return total number of tokens
        """
        return len(self.tokens)
    
    def get_vocab_size(self):
        """
        Return size of vocabulary (unique words)
        """
        return len(self.word_freq)

# Example usage
def main():
    # Create tokenizer instance
    tokenizer = Tokenizer()
    
    # Sample text
    sample_text = "Hello world! This is a test. Hello again, world!"
    
    # Tokenize the text
    tokens = tokenizer.tokenize(sample_text)
    
    # Print results
    print("Tokens:", tokens)
    print("Vocabulary:", tokenizer.get_vocabulary())
    print("Word Frequencies:", tokenizer.get_word_frequency())
    print("Total Token Count:", tokenizer.get_token_count())
    print("Vocabulary Size:", tokenizer.get_vocab_size())

if __name__ == "__main__":
    main()