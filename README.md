
# Machine Learning-Based Web Application Firewall (WAF)

## Overview
This project implements a Web Application Firewall (WAF) that detects and prevents Cross-Site Scripting (XSS) attacks, which are a common threat to web applications. Using a Support Vector Machine (SVM) model, the WAF processes incoming HTTP requests, classifies them as either benign or malicious, and accurately identifies the type of attack if one is detected. The system achieved an accuracy of 99.58% in identifying these attacks.

## Features:
- Detects Cross-Site Scripting (XSS) attacks in real time.
- Classifies incoming HTTP requests based on attack types.
- Achieves high classification accuracy (99.58%).
- Utilizes a Support Vector Machine (SVM) model for efficient classification.
- Data preprocessing and feature extraction for optimized performance.

## Requirements:
- Python 3.x
- Scikit-learn
- Pandas
- NumPy
- Flask (if implementing the WAF as a web service)

## Installation Instructions:
1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/waf-ml.git
   ```
2. Install the required dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebooks in the `notebooks/` folder to preprocess the data, train the model, and evaluate it.

4. Start the WAF as a Flask service:
   ```bash
   cd waf/
   python app.py
   ```

## Usage:
- To test the WAF, send HTTP requests to the Flask server. The request will be classified as benign or an XSS attack.
- The firewall logs the results of each request and can block malicious traffic.

## Project Description:
Cross-Site Scripting (XSS) attacks are dangerous vulnerabilities that allow attackers to inject malicious scripts into web pages viewed by users. The goal of this project is to develop a Web Application Firewall that can prevent such attacks using a machine learning model.

This WAF is built using a Support Vector Machine (SVM), a powerful algorithm for classification tasks. The project involves the following key steps:

1. **Data Preprocessing:**  
   The dataset of HTTP requests is cleaned and preprocessed to extract relevant features (such as query parameters, request headers, and payloads) that could indicate an XSS attack. Common preprocessing techniques such as tokenization, encoding, and normalization are applied to prepare the data for model training.

2. **Model Building:**  
   Using the preprocessed data, an SVM classifier is trained to detect and classify XSS attacks. The model is fine-tuned to optimize its performance, achieving an impressive accuracy of 99.58%. The classifier can identify various attack types, such as reflected, stored, and DOM-based XSS attacks.

3. **Model Evaluation:**  
   The performance of the model is evaluated using accuracy, precision, recall, and F1-score. The model demonstrates high accuracy in classifying benign and malicious requests, with a particular focus on minimizing false positives to avoid blocking legitimate traffic.

4. **Implementation of the WAF:**  
   The trained SVM model is integrated into a Flask-based web service. Incoming HTTP requests are analyzed in real time, and the model classifies each request. If an attack is detected, the firewall takes appropriate action (such as blocking the request or alerting the admin).

5. **Results:**  
   The system successfully detects and blocks XSS attacks with an accuracy of 99.58%. It demonstrates robustness in real-time traffic scenarios, ensuring the security of web applications.

## Contributors:
- Prajwal

## License:
This project is licensed under the MIT License.
