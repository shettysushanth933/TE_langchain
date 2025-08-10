##SkillBridgeAI: Intelligent Resume & Job Description Analyzer
<p align="center">
<img src="https://img.shields.io/badge/Python-3.9%2B-blue.svg" alt="Python Version">
<img src="https://img.shields.io/badge/Framework-Streamlit-red.svg" alt="Framework">
<img src="https://img.shields.io/badge/API-Google%20Gemini-purple.svg" alt="API">
<img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

SkillBridgeAI is a sophisticated Streamlit web application designed to bridge the gap between job seekers and their dream jobs. By leveraging the power of Google's Gemini 1.5 Flash model, it provides a multi-faceted analysis of a user's resume against a specific job description.

The application offers instant, AI-driven feedback, helping candidates understand their strengths, identify skill gaps, and receive actionable advice to improve their application, all within a sleek, modern, and theme-able user interface.

-----

## ✨ Core Features

SkillBridgeAI is organized into five distinct analysis tabs, each providing unique insights:

  * **📈 Job Role Fit:** Get an overall prediction of your suitability for a role, including a percentage score and a detailed breakdown of your strengths and areas for improvement.
  * **🔍 Skill Gap Analysis:** The app intelligently identifies which skills you're missing for a target job and categorizes them as *Critical*, *Important*, or *Nice-to-Have*.
  * **📚 Personalized Course Recommendations:** To help you bridge the skill gaps, the app suggests specific, high-quality courses and resources from popular learning platforms.
  * **📄 In-Depth Resume Review:** Receive feedback from an AI expert acting as an HR manager. Your resume gets a score out of 10, along with actionable recommendations to make it stand out.
  * **🎯 ATS-Style Percentage Match:** See a high-level percentage match score broken down by key areas like Technical Skills, Experience, and Education, simulating how an Applicant Tracking System (ATS) might view your profile.
  * **🎨 Dual-Theme UI:** A beautifully crafted interface with both **Light** and **Dark** modes for a comfortable user experience.

-----

## 🏗️ How It Works

The application follows a simple yet powerful architecture:

1.  **Frontend Interface (Streamlit):** The user-friendly interface is built with Streamlit. It allows users to select a job role, input their skills, upload their resume (PDF), and paste a job description.
2.  **PDF Processing (`pdf2image`):** When a PDF resume is uploaded, the application's backend converts the **first page** of the PDF into a JPEG image. This allows the multimodal Gemini model to "read" the resume's layout and content visually.
3.  **AI-Powered Analysis (Google Gemini):** The user's inputs, the job description, and the resume image are sent to the **Gemini 1.5 Flash API**. A series of carefully crafted, role-specific prompts guide the model to perform the analyses for each tab.
4.  **Dynamic Output:** The model's response is streamed back and displayed in a clean, well-formatted markdown format within the corresponding tab, providing instant and valuable feedback.

-----

## 🛠️ Setup and Installation

Follow these steps to get SkillBridgeAI running on your local machine.

### Prerequisites

  * **Python 3.9+** and **pip**
  * **Git**
  * **Poppler:** This is a dependency for `pdf2image` to work correctly.
      * **Windows:** Download the latest release from [this blog](https://www.google.com/search?q=https://blog.alivate.com.au/poppler-windows/) and add the `bin` directory to your system's PATH.
      * **macOS (using Homebrew):**
        ```bash
        brew install poppler
        ```
      * **Linux (Debian/Ubuntu):**
        ```bash
        sudo apt-get install -y poppler-utils
        ```

### Installation Steps

1.  **Clone the Repository:**

    ```bash
    git clone https://github.com/shettysushanth933/TE_langchain.git
    cd SkillBridgeAI
    ```

2.  **Create a Virtual Environment:**
    It's highly recommended to use a virtual environment to manage dependencies.

    ```bash
    python -m venv venv
    ```

      * **Activate on Windows:**
        ```bash
        .\venv\Scripts\activate
        ```
      * **Activate on macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```

3.  **Install Dependencies:**
    Create a `requirements.txt` file with the following content:

    ```txt
    streamlit
    google-generativeai
    python-dotenv
    pdf2image
    Pillow
    ```

    Then, install the packages:

    ```bash
    pip install -r requirements.txt
    ```

4.  **Set Up Environment Variables:**
    You'll need a Google Gemini API key. You can get one from [Google AI Studio](https://aistudio.google.com/app/apikey).

      * Create a file named `.env` in the root of your project directory.
      * Add your API key to this file:
        ```
        GOOGLE_API_KEY="YOUR_API_KEY_HERE"
        ```

5.  **Run the Application:**
    Once everything is set up, run the following command in your terminal:

    ```bash
    streamlit run app.py
    ```

    Your browser should automatically open to the application's local URL.

-----

## 🚀 Usage

Using the app is straightforward:

1.  **Select Your Job Role:** Choose the job you're applying for from the dropdown menu.
2.  **Select Your Skills:** Pick the skills you possess from the multiselect box.
3.  **Upload Your Resume:** Click the file uploader to select and upload your resume in PDF format.
4.  **Paste the Job Description:** Copy the full job description from a listing and paste it into the text area.
5.  **Navigate the Tabs:** Click on any of the five analysis tabs ("Job Role Fit", "Skill Gap Analysis", etc.).
6.  **Generate Analysis:** Click the button within each tab (e.g., "Predict Fit") to generate the AI-powered analysis for that specific category.

-----

## 📂 Project File Structure

```
SkillBridgeAI/
├── .env                  # Stores your API key (not version controlled)
├── app.py                # Main Streamlit application script
├── requirements.txt      # List of Python dependencies
└── README.md             # You are here!
```

-----

## 🤝 Contributing

Contributions are welcome\! If you have suggestions for improvements or want to add new features, please feel free to fork the repository, make your changes, and submit a pull request.

-----

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.



