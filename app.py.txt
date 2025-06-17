import streamlit as st
import joblib
import re

# Clean input text
def clean_text(text):
    text = re.sub(r'http\S+', '', text)
    text = re.sub(r'[^A-Za-z0-9\s]', '', text)
    text = text.lower()
    return text

# Load ML model and vectorizer
model = joblib.load("fake_news_model.pkl")
vectorizer = joblib.load("tfidf_vectorizer.pkl")

# Streamlit app
st.title("📰 Fake News Detector")
st.subheader("Enter news content or headline to check if it's real or fake.")

user_input = st.text_area("✍️ Paste the news text here:")

if st.button("Check"):
    cleaned = clean_text(user_input)
    input_vector = vectorizer.transform([cleaned])
    prediction = model.predict(input_vector)[0]

    if prediction == 1:
        st.success("✅ This looks like *Real News*")
    else:
        st.error("❌ This looks like *Fake News*")
