# html_to_text
Library to create shorter and clean text to searching the keywords

## Hints
https://stackoverflow.com/questions/5454235/shorten-string-without-cutting-words-in-javascript


    If I understand correctly, you want to shorten a string to a certain length (e.g. shorten "The quick brown fox jumps over the lazy dog" to, say, 6 characters without cutting off any word).

    If this is the case, you can try something like the following:

    var yourString = "The quick brown fox jumps over the lazy dog"; //replace with your string.
    var maxLength = 6 // maximum number of characters to extract

    //trim the string to the maximum length
    var trimmedString = yourString.substr(0, maxLength);

    //re-trim if we are in the middle of a word
    trimmedString = trimmedString.substr(0, Math.min(trimmedString.length, trimmedString.lastIndexOf(" ")))
