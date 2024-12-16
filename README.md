# First, install the langdetect library if you haven't already
# You can install it using pip:
# pip install langdetect

from langdetect import detect, detect_langs

def detect_language(text):
    try:
        # Detect the language of the text
        language = detect(text)
        # Detect the probabilities of all languages
        languages_prob = detect_langs(text)
        return language, languages_prob
    except Exception as e:
        return str(e)

# Example usage
text = "Bonjour tout le monde"
language, languages_prob = detect_language(text)
print(f"Detected language: {language}")
print(f"Language probabilities: {languages_prob}")
