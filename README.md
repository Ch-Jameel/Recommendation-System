# TED Talk Recommender

## Objective

The TED Talk Recommender is a Python project designed to recommend related transcripts based on text similarity. The primary goal is to enhance user engagement and content discovery within TED Talks.

## How It Works

1. **Text Preprocessing:**
   - Utilize NLTK to preprocess subtitle and transcript data.
   - Apply the `preprocess_text` function for lowercasing, punctuation removal, stop word elimination, and lemmatization.

2. **TF-IDF Matrix Creation:**
   - Use scikit-learn's TfidfVectorizer to create a TF-IDF matrix.
   - Generate TF-IDF weights from the preprocessed "Subtitle" column.

3. **Cosine Similarity:**
   - Compute the cosine similarity matrix between "Subtitle" TF-IDF and "transcript" vectorized columns.

4. **Recommendation Function:**
   - The `recommend_transcripts` function takes a subtitle, cosine similarity matrix, and transcript data.
   - Identifies the subtitle's row index in the cosine similarity matrix.
   - Retrieves similarity scores, sorts, and selects top transcripts.
   - Returns a list of top transcripts' URLs and corresponding transcripts.
