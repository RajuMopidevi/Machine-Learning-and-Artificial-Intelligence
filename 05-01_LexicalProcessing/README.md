1. NLP Lexical Processing
    1. Introduction to NLP
        1. Introduction
            - Text analytics(NLP) plays a very vital role in today’s era because of the sheer volume of text data that users generate around the world on digital channels such as social media apps, e-commerce websites, blog posts, etc
        2. NLP: Areas of Application
            1. Social Media Analytics
            2. Banking and loan Processing
            3. Insurance claim processing
            4. Customer relationship processing
            5. Security and counter-terrorism
            6. Computational social science
            7. E-Commerce
            8. Psychology and cognitive science
        3. Understanding Text
            * ![Flow](https://github.com/RajuMopidevi/Machine-Learning-and-Artificial-Intelligence/blob/main/05-01_LexicalProcessing/05-01_NLP_01.png?raw=true)
            * **Lexical Processing**: 
                - convert the raw text --> words --> sentences or paragraphs
                - In general, we can consider all plural words to be equivalent to the singular form.
                - Lexical processing will treat the two sentences as equal if the “group of words” in both sentences are the same.
            * **Syntactic Processing**:
                - Instead of only looking at the words, we look at the syntactic structures, i.e., the grammar of the language
                - Ex: Differentiating between the subject and the object of the sentence, i.e., identifying who is performing the action and who is the person affected by it
                - A question answering system. Ex: Who is the Prime Minister of India?
            * **Semantic Processing**: 
                - Lexical and syntactic processing don't suffice when it comes to building advanced NLP applications such as language translation.
                - inferring the word’s meaning to the collection of words that usually occur around it.
                - Understand other semantic relations. Ex: King and Queen are related. Both of these words can be clubbed under the word “Monarch”
            * Most of the applications, lexical and semantic processing simply form the “pre-processing” layer of the overall process.
        4. Text Encoding
            - Computers could handle numbers directly and store them on registers (the smallest unit of memory on a computer). But they couldn’t store the non-numeric characters as is. The alphabets and special characters were to be converted to a numeric value first before they could be stored
            - All the non-numeric characters were **encoded** to a number using a code
            - The first encoding standard that came into existence was the **ASCII (American Standard Code for Information Interchange)** standard, in 1960.
            - **Unicode standard** supports all the languages in the world - both modern and the older ones.
            - Before even beginning with any text processing, you need to know what kind of encoding the text has and if required, modify it to another encoding format.
            - Encoding: ![table](https://github.com/RajuMopidevi/Machine-Learning-and-Artificial-Intelligence/blob/main/05-01_LexicalProcessing/encoding.png?raw=true)
            - The default encoding for strings in python is Unicode UTF-8.
            - ```python
                # create a string
                amount = u"₹50"
                print('Default string: ', amount, '\n', 'Type of string', type(amount), '\n')

                # encode to UTF-8 byte format
                amount_encoded = amount.encode('utf-8')
                print('Encoded to UTF-8: ', amount_encoded, '\n', 'Type of string', type(amount_encoded), '\n')
                ```
        5. Regular expressions: Quantifiers - I
            - A regular expression is a set of characters, or a pattern, which is used to find substrings in a given string
            - Regulars expressions are a language in itself since they have their own compilers
            - Used for feature extraction from text, string replacement and other string manipulations
            - The `re.search()` method returns a RegexObject if the pattern is found in the string, else it returns a None object
            - `re.search(pattern, string).start()` and `re.search(pattern, string).end()` will return the index of the starting and ending position of the match found.
            - Quantifiers allow you to mention and have control over how many times you want the character(s) in your pattern to occur.
            - four types of quantifiers:
                1. **The ‘?’ operator** : The ‘?’ matches the preceding character zero or one time. It is generally used to mark the **optional presence** of a character.
                2. **The ‘*’ operator** : The ‘*’ quantifier is used to mark the presence of the preceding character **zero or more times**.
                3. **The ‘+’ operator** : The ‘+’ quantifier matches the preceding character one or more times.
                4. **The ‘{m, n}’ operator** : This will match occurrences of the preceding character a fixed number of times
             - The only difference between '+' and '*' is that the '+' needs a character to be present at least once, while the '*' does not
        6. Regular expressions: Quantifiers - II
            + There are four variants of the quantifier :
                - {m, n}: Matches the preceding character ‘m’ times to ‘n’ times.
                - {m, }: Matches the preceding character ‘m’ times to infinite times, i.e. there is no upper limit to the occurrence of the preceding character.
                - {, n}: Matches the preceding character from zero to ‘n’ times, i.e. the upper limit is fixed regarding the occurrence of the preceding character.
                - {n}: Matches if the preceding character occurs exactly ‘n’ number of times.
            + '?' is equivalent to zero or once, or {0, 1}
            + '*' is equivalent to zero or more times, or {0, }
            + '+' is equivalent to one or more times, or {1, }
        7. Comprehension: Regular Expressions
            - A whitespace comprises of a single space, multiple spaces, tab space or a newline character (also known as a vertical space)
            - **The parentheses** :The quantifier will look for repetition of the group of characters rather than just looking for repetitions of the preceding character. This concept is called grouping in regular expression jargon
            - **The pipe operator**: It’s notated by ‘|’. The pipe operator is used as an OR operator. You need to use it inside the parentheses
            - **The escape sequence** : It is denoted by a backslash ‘\’, is used to escape the special meaning of the special characters
        10. Regular Expressions: Anchors and Wildcard
        11. Regular Expressions: Characters Sets
        12. Greedy versus Non-greedy Search
        13. Commonly Used RE Functions
        14. Regular Expressions: Grouping
        15. Regular Expressions: Use Cases
        16. Summary
    2. Basic Lexical Processing
        1. Introduction
        2. Word Frequencies and Stop Words
        3. Tokenisation
        4. Bag-of-Words Representation
        5. Stemming and Lemmatization
        6. Final Bag-of-Words Representation
        7. TF-IDF Representation
        8. Building a Spam Detector-I
        9. Building a Spam Detector-II
        10. Summary
    3. Advanced Lexical Processing
        1. Introduction
        2. Canonicalisation
        3. Phonetic Hashing
        4. Edit Distance
        5. Spell Corrector - I
        6. Spell Corrector - II
        7. Pointwise Mutual Information - I
        8. Pointwise Mutual Information - II
        9. Summary
