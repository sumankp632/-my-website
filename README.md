Real-Time Language Translation Using Neural Machine Translation (NMT)
🚀 A multilingual translation model using the mT5 Transformer to break language barriers in real-time.



📌 Overview
This project implements a real-time translation system using the mT5-base model from Hugging Face. It can translate text between multiple languages, such as English (en), Japanese (ja), and Chinese (zh). The model is fine-tuned on a multilingual dataset and optimized for accurate translation.


🚀 How It Works
1️⃣ Tokenization
The input text is first tokenized using the mT5-base tokenizer and preprocessed.

python
Copy
Edit
input_ids = tokenizer.encode(
    '<zh> Hello, how are you?', return_tensors="pt", padding=True, truncation=True
)
2️⃣ Model Inference
The encoded input is passed through the mT5 model to generate the translation.

python
Copy
Edit
output_tokens = model.generate(input_ids, num_beams=5)
3️⃣ Decoding
The generated output tokens are converted back into human readable text.

python
Copy
Edit
translated_text = tokenizer.decode(output_tokens[0], skip_special_tokens=True)
print("Translation:", translated_text)
📊 Evaluation & Results
The model was tested using BLEU and ROUGE scores for translation accuracy.
Example output:

css
Copy
Edit
Input: "What is your name?"
Output (Chinese): "你的名字是什么?"
📌 Features
✅ Supports English, Japanese, and Chinese
✅ Uses mT5 Transformer for high-quality translation
✅ Implements Beam Search for better accuracy
✅ GPU acceleration with CUDA support

📌 Future Enhancements
🔹 Expand language support (e.g., Spanish, German)
🔹 Deploy as an API or web app
🔹 Improve translation fluency with fine-tuning

📝 Contributors
Vandhana – Model Training & Evaluation,
Ridhin – Data Preprocessing & Tokenization,
Shiva – Model Inference & Testing,
Angel – UI & Documentation
📜 License
This project is licensed under the MIT License.
