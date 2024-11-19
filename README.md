# YouTube-Recommendation-System
In the **YouTube Recommendation System** project, you developed a **content-based filtering system** to recommend videos based on a user's watch history. Here's a step-by-step summary of what you've done:  

### 1. **Dataset Extraction**  
- You extracted your YouTube watch history data from **Google Takeout**, which provided a JSON file containing details like video titles, channel names, timestamps, and more.
- This data was converted into a CSV format for easier processing and analysis.

---

### 2. **Data Preprocessing**  
- **Cleaning and Handling Missing Data**:
  - Extracted meaningful information, like video titles and channel names.
  - Removed unnecessary parts from titles for better text analysis.
  - Filled missing channel names with a placeholder ("unknown").
- **Feature Engineering**:
  - Combined the `title` and `channelname` columns into a single feature (`combined_features`) to create a richer representation of each video.

---

### 3. **Content-Based Filtering Implementation**  
- **TF-IDF Vectorization**:
  - Applied **TF-IDF (Term Frequency-Inverse Document Frequency)** to the `combined_features` column to convert textual data into numerical vectors. This step quantified the importance of words in each video description relative to others.
- **Cosine Similarity**:
  - Computed the **cosine similarity** between all videos to measure their similarity based on their vector representations. This similarity metric ranges between 0 (no similarity) and 1 (perfect similarity).

---

### 4. **Recommendation Function**  
- Built a function to:
  - Retrieve a video based on its index in the dataset.
  - Find and sort the most similar videos using the cosine similarity matrix.
  - Display the top 5 recommended videos for a selected video.

---

### 5. **Visualization**  
- **Heatmap of Cosine Similarity**:
  - Visualized similarity scores between videos using a heatmap, showing how closely related each video is to others.
- **Bar Plot of Top Recommendations**:
  - Created bar plots displaying the top recommended videos for a specific video, including their cosine similarity scores for easy interpretation.

This project demonstrates a complete pipeline for a recommendation system using real-world data, applying natural language processing, machine learning techniques, and effective visualization to deliver actionable insights.
