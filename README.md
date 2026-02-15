# MLPR-llab-5 
## Face Classification using HSV Colour Features and K-Means Clustering

---

## Objective

The objective of this lab is to design a simple face grouping and classification system using colour-based features. Instead of relying on high-dimensional features, this experiment explores the use of **Hue and Saturation (HSV colour space)** as low-dimensional descriptors and applies **K-Means clustering** for grouping detected faces. A template image is then classified based on learned cluster centroids.

---

## Experimental Approach

The implementation is divided into the following stages:

### 1. Face Detection
- Faces are detected using the **Haar Cascade classifier**.
- Detection is performed on grayscale images.
- Bounding boxes are generated to isolate facial regions for further processing.

---

### 2. Feature Engineering (HSV-Based Representation)
- Each detected face region is converted from **BGR colour space to HSV colour space**.
- The **mean Hue (H)** and **mean Saturation (S)** values are computed.
- These two values form a compact 2D feature vector representing each face.

This reduces dimensionality while preserving meaningful colour information.

---

### 3. Unsupervised Clustering with K-Means
- All extracted (H, S) feature vectors are grouped using **K-Means clustering**.
- Number of clusters: **K = 2**
- Cluster centroids are computed and visualized in feature space.

This step separates faces into clusters based on colour similarity.

---

### 4. Template Face Classification
- A separate template image undergoes the same pipeline:
  - Face detection  
  - HSV conversion  
  - Mean Hue–Saturation extraction  
- The resulting feature vector is assigned to the nearest cluster centroid.

Classification is therefore performed using a **distance-based decision rule**.

---

## Results and Visual Evidence

### Face Detection
Detected faces are enclosed within bounding boxes.



---

### Hue–Saturation Feature Distribution
The extracted features are visualized in 2D HS-space along with cluster centroids.



---

### Template Classification
The template face is plotted alongside clustered data points to illustrate its assigned group.



---

## Observations

- HSV colour representation provides a simple yet effective feature space.
- Even with only two features, K-Means forms distinguishable clusters.
- Cluster visualization improves interpretability of the classification decision.
- Distance-based assignment works effectively when clusters are well-separated.

---

## Conclusion

This experiment demonstrates how unsupervised learning can be applied to image-based classification tasks using minimal features. By combining:

- Classical face detection  
- Colour-space transformation  
- Low-dimensional feature extraction  
- K-Means clustering  

a functional classification pipeline can be constructed without labeled training data.

The lab highlights the importance of feature selection and visualization in pattern recognition problems.

---

## Technologies Used

- Python  
- OpenCV  
- NumPy  
- Matplotlib  
- Scikit-learn  



## Repository Structure


<img width="602" height="400" alt="FACULTY" src="https://github.com/user-attachments/assets/8cccf630-4ba9-4d02-b517-187286272d16" />


![Dr_Shashi_Tharoor](https://github.com/user-attachments/assets/10d887df-0956-4cfe-a098-c354b15c7866)

<img width="619" height="340" alt="picture" src="https://github.com/user-attachments/assets/6fab7811-b9a8-421a-8412-ce3427117e6c" />


<img width="685" height="364" alt="Screenshot 2026-02-15 224456" src="https://github.com/user-attachments/assets/169e15e8-7526-4cc8-9a5d-6b530b4278a7" />

<img width="624" height="344" alt="Screenshot 2026-02-15 210728" src="https://github.com/user-attachments/assets/8e15fe74-e9fa-459c-86ce-9b54449aebae" />

