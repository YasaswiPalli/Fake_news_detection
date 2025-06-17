# 📰 Fake News Detection

A simple machine learning web app built using **Python**, **Scikit-learn**, and **Streamlit** to detect whether a news headline or article is *Fake* or *Real*.

![Streamlit Screenshot](https://user-images.githubusercontent.com/your-image-here.png)

---

## 🚀 Live Demo

Try the app here: [Streamlit Deployment Link](https://your-streamlit-app-link.streamlit.app)

---

## 📁 Project Structure


---

## 🔍 How It Works

1. The app uses a **TF-IDF Vectorizer** to transform the input news text.
2. A trained **Logistic Regression model** (or any other classifier) then predicts if the news is real or fake.
3. The result is shown in a clean and interactive Streamlit UI.

---

## 🧪 Example Inputs

- ✅ *Real:* `"Donald Trump wins the 2016 U.S. presidential election."`
- ❌ *Fake:* `"Pope Francis shocks world, endorses Donald Trump for President."`

---

## 📦 Installation & Running Locally

```bash
# 1. Clone the repository
git clone https://github.com/YasaswiPalli/Fake_news_detection.git
cd Fake_news_detection

# 2. (Optional) Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate  # On Windows

# 3. Install required libraries
pip install -r requirements.txt

# 4. Run the app
streamlit run app.py

pip install -r requirements.txt
