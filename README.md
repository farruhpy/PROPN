# PROPN
A program that extracts certain types of nouns from input text that are required or should be output (Proper nouns in this case)


--------

``Proper Nouns Identification Program''
FIRST OF ALL, TO RUN THIS PROGRAM, THE LAPTOP OR COMPUTER MUST HAVE SPACY, en_core_web_sm, AND googletrans 4.0.0-rc1 LIBRARIES INSTALLED!!!

The program performs three functions. These are: translate_uzbek_to_english, translate_english_to_uzbek and spacy_func.

1. translate_uzbek_to_english: This function takes a text string in Uzbek as input and returns the translated text to English. It uses the Translator class from the googletrans library to do the translation.

2. translate_english_to_Uzbek: This function is similar to the previous one, but instead translates the text from English to Uzbek.

3. spacy_func: This function takes a text string in Uzbek as input and returns a list of nouns in the text translated into Uzbek.

Here's how it works:
 A. It translates input text from Uzbek to English using the translate_uzbek_to_english function.

 B. It loads the English model from Spacy using spacy.load("en_core_web_sm").

 C. It processes the translated text using the Spacy model and outputs the first sentence.

 D. It iterates over each token in the sentence and checks that the token's part of speech is a valid noun (specified by PROPN).

 E. If the lexeme is a valid noun, it is translated into Uzbek using the translate_english_to_Uzbek function and added to the list of nouns.

 F. Finally, it returns a list of translated proper nouns.

At the end of the program, the list of famous words in the given sentence is printed in the output part. For example, if we call the spacy_func function and write to it "Amir Temur was born in Shahrisabz on April 9", it will return a list of famous names ['Amir', 'Temur', 'April', 'Shahrisabz'].
