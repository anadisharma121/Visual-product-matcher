# Visual Product Matcher

A web application that allows users to find visually similar products by uploading an image or providing an image URL.

## Features
- Upload image via file or URL
- MobileNetV2-based feature extraction
- Visual similarity search with cosine similarity
- Filter results by similarity score
- Displays product metadata with images
- Responsive and clean UI using Bootstrap and custom styles

## Technologies
- Python, Flask
- TensorFlow (MobileNetV2)
- Pandas, NumPy, scikit-learn
- Bootstrap CSS for frontend

## Approach
The Visual Product Matcher project creates a complete system for finding visually similar products. It does this by using deep-learning image features along with a simple web interface. The process starts with data preparation, which includes cleaning metadata, downloading product images, and resizing them to meet the model's requirements. A pretrained MobileNetV2 convolutional neural network serves as the feature extractor, producing high-dimensional features that capture key visual traits of each product image. These features are calculated once for the entire catalog and stored for quick access. When a user uploads an image or provides an image URL, the system processes the query using the same CNN to get its feature and then calculates cosine similarity between that feature and the stored catalog features. The results are ranked by similarity score, filtered, and shown along with product information to allow easy comparison. The backend is built with Flask, while the frontend uses HTML, Bootstrap, and custom CSS for a clean, responsive layout. This modular design, which separates data preparation, feature extraction, and inference, makes the system easy to maintain and extend. While it works well for small to medium datasets, the project can be enhanced by adding approximate nearest neighbor search for better scalability, adjusting the model for specific kinds of similarity, or including multimodal features like product descriptions. Overall, the project shows a practical and effective method for searching visual similarities, demonstrating how pretrained CNN features and straightforward similarity metrics can be used to create real-world product discovery tools.

## Deployed Link
[Visual Product Matcher](https://visual-product-matcher-1-ckgm.onrender.com)

## Setup and Installation

1  git clone <repo_url>         
 Download the project repository to local machine

2  cd <repo_folder>             
 Change directory to the project folder

3 python -m venv venv          
 Create a virtual environment named 'venv' for dependency isolation

4 source venv/bin/activate     
 Activate the virtual environment (on Windows: venv\Scripts\activate)

5 pip install -r requirements.txt  
 Install all required Python packages listed in requirements.txt

6 python app.py                
 Run the Flask web application locally

## Contributor
Anadi Sharma
