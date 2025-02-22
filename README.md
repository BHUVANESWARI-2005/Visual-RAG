# Conversational Image Recognition Chatbot

# **Overview**

This project utilizes OpenAI's CLIP (Contrastive Language-Image Pretraining) model to encode images into embeddings, build a searchable image database, and retrieve the most similar images based on cosine similarity. It enables:

-Image-to-Image Search (Finding the closest match for a query image)

-Image Retrieval by Description or Label

-Cosine Similarity Scoring for Image Comparisons

-Visualization of Retrieved Images


# **Features :**

✅ Encode images into CLIP embeddings

✅ Build a searchable image database with descriptions & labels

✅ Find the closest image match using cosine similarity

✅ Search for images using descriptions or labels

✅ Display retrieved images using Matplotlib

✅ Print similarity scores for all images in the database



# **Implementation Details**


**1. Model and Libraries Used**

CLIP (Contrastive Language-Image Pretraining): Used for encoding images into feature vectors.

Scikit-learn (cosine similarity): Computes similarity between embeddings.

PIL (Python Imaging Library): Handles image loading and processing.

Matplotlib: Displays retrieved images.

Pickle: Saves and loads the image database.


**2. Image Encoding**

The encode_image(image_path) function uses CLIP to convert an image into a normalized feature vector.


**3. Database Construction**

The build_database(image_paths, descriptions, labels, database_path) function encodes each image and stores its embedding along with its description, label, and path.

The database is saved as a pickle file.


**4. Image Retrieval**

By Image Similarity:

find_closest_match(query_image_path, database): Computes cosine similarity between the query image and images in the database to find the closest match.

By Text Query (Description or Label):

find_image_by_description_or_label(query, database): Searches for images matching a given description or label.


**5. Cosine Similarity Computation**

calculate_cosine_similarity(database, query_image_path): Computes similarity scores for all images in the database.


**6. Best Match Retrieval**

find_best_match(database, query_image_path, labels): Finds the best-matching image based on similarity scores and returns the label and score


# **Technologies Used**

-Python

-PyTorch

-Transformers (Hugging Face)

-CLIP (OpenAI)

-BLIP (Salesforce)

-Scikit-learn (K-Means for color detection)

-Gradio (for UI)
