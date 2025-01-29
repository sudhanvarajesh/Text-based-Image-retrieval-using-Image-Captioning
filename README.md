# **Text-based Image Retrieval Using Captioning**  

![Tech Stack](https://img.shields.io/badge/Tech%20Stack-Python%20%7C%20Deep%20Learning%20%7C%20VGG16%20%7C%20GRU%20%7C%20BM25-blue)  

## **Overview**  
Retrieving relevant images from a large database is often time-consuming. Conventional methods rely on manually generated metadata, which is inefficient. This project automates image retrieval by leveraging **image captioning with an attention mechanism** to generate descriptive annotations for images. A **BM25 ranking system** then compares user queries with these captions to retrieve the most relevant images.  

## **Features**  
✅ **Automated Image Captioning** – Generates textual descriptions using a CNN-RNN model with **Bahdanau Attention**.  
✅ **Efficient Image Retrieval** – Uses **BM25 ranking** to match user queries with generated captions.  
✅ **VGG16-Based Feature Extraction** – Extracts visual features for improved captioning accuracy.  
✅ **Active Learning Mechanism** – Allows the system to improve over time based on user feedback.  
✅ **Scalable Image Search** – Supports large datasets like Flickr8k for real-world applications.  

## **Tech Stack**  
- **Deep Learning:** TensorFlow, Keras  
- **Feature Extraction:** VGG16 (CNN)  
- **Caption Generation:** GRU (Gated Recurrent Unit) with Attention  
- **Text Search & Ranking:** BM25 (Okapi)  
- **Dataset Used:** Flickr8k  

## **Dataset**  
The project uses the **Flickr8k dataset**, which contains 8,000 images with five captions per image.  
🔗 **Dataset Link:** [Flickr8k](https://drive.google.com/drive/folders/1i5ZRdB5kOOJ1OOBlc1rpvoMDGLbupOsM?usp=sharing)  

- **Images Folder:** `Flicker8k_Dataset/`  
- **Pre-generated Captions:** `data.json` (Used for inference without retraining)  

## **Installation & Setup**  

### **Prerequisites**  
Ensure you have the following installed:  
- [Python 3](https://www.python.org/downloads/)  
- [Jupyter Notebook](https://jupyter.org/install) *(Recommended for experimentation)*  

### **Setup**  
1. **Clone the repository**  
   ```sh
   git clone https://github.com/sudhanvarajesh/Text-based-Image-retrieval-using-Image-Captioning
   cd Text-based-Image-Retrieval
   ```

2. **Install dependencies**  
   ```sh
   pip install -r requirements.txt
   ```

3. **Download the dataset** ([Google Drive Link](https://drive.google.com/drive/folders/1i5ZRdB5kOOJ1OOBlc1rpvoMDGLbupOsM?usp=sharing)) and place it in the project directory under `Flicker8k_Dataset/`.  

4. **Run the Jupyter notebook** to train the model and generate captions  
   ```sh
   jupyter notebook
   ```

5. **Run the server**  
   ```sh
   python server.py
   ```

## **Usage**  
- **Train the captioning model** using the provided Jupyter notebook.  
- **Generate and store image captions** in a JSON file (`data.json`).  
- **Run the retrieval system** to match input queries with captions using BM25.  
- **Upload images** via the web interface and retrieve related images based on captions.  

## **Demo**  
🔗 **Video Demo:** *(https://drive.google.com/file/d/1ocgiXuJMIZt5jnyTM-gKvQha7tGb9Q9i/view?usp=drive_link)*  

## **Results**  
📌 **Captioning Accuracy:** Achieved **0.663 cosine similarity** on the Flickr8k validation set.  
📌 **Image Retrieval Accuracy:** Retrieved the correct image **61% of the time**, with close matches otherwise.  

## **Future Improvements**  
🔹 **Use a larger dataset like MS-COCO** to improve captioning quality.  
🔹 **Optimize BM25 ranking** for better query matching.  
🔹 **Implement reinforcement learning** to refine captioning accuracy over time.  

## **Contributing**  
Contributions are welcome! To contribute:  
1. **Fork the repository**  
2. **Create a new branch** (`feature/your-feature`)  
3. **Commit your changes**  
4. **Open a pull request**  
