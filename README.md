
CLIP Image & Text Search API

Welcome to the CLIP Image & Text Search API! This project is an exciting tool that lets you search for images using either text (like "A cute cat") or by uploading another image. It’s powered by a FastAPI backend that uses OpenAI's CLIP model and Pinecone vector search to deliver fast and accurate results. Paired with a sleek Streamlit frontend, it’s designed to be both powerful and user-friendly.

Table of Contents

What’s This Project About?

Cool Features
How It’s Organized
What You’ll Need
Step-by-Step Setup Guide
Running the App
Deploying It Online
How to Use It
Want to Help Out?
License

What’s This Project About?

The CLIP Image & Text Search API is all about making image searching simple and smart. The backend, built with FastAPI, handles your search requests lightning-fast. It uses OpenAI’s CLIP model to turn text and images into something a computer can understand (embeddings), and Pinecone helps store and find them quickly. The Streamlit frontend gives you a clean, interactive way to try it out—whether you’re typing a description or uploading a picture.

Cool Features

Image-to-Image Search: Upload a photo and find others that look similar.
Text-to-Image Search: Type "sunset beach" and see matching images.
Pinecone Power: Stores and searches image data super efficiently.
CLIP Magic: Uses openai/clip-vit-base-patch32 to create top-notch embeddings.
FastAPI Backbone: A speedy API keeps everything running smoothly.
Streamlit Interface: A slick, easy-to-use frontend for searching.
Ready to Scale: Deploy it easily on platforms like Heroku or Render.
How It’s Organized

Here’s a peek at the project’s folder structure:

image-processing-app/
├── backend/                # The FastAPI backend
│   ├── models/             # Data models
│   │   └── image_search.py # Defines the API response structure
│   ├── services/           # Core logic
│   │   └── search_service.py # Handles embedding and search tasks
│   ├── search/             # API endpoints
│   │   └── endpoints.py    # Defines the search routes
│   ├── .env                # Stores secrets like the Pinecone API key
│   ├── main.py             # The FastAPI app entry point
│   ├── requirements.txt    # Backend dependencies
│   └── README.md           # Backend-specific notes
├── frontend/               # The Streamlit frontend
│   ├── app.py              # The Streamlit UI code
│   ├── requirements.txt    # Frontend dependencies
│   └── README.md           # Frontend-specific notes
├── .gitignore              # Files to ignore in Git
└── README.md               # You’re reading it!

What You’ll Need

Before you dive in, make sure you have:

An operating system: Windows, macOS, or Linux.
Python 3.10+ (check with python --version—it should be 3.10 or higher).
Git (grab it from git-scm.com).
pip (comes with Python; confirm with pip --version).
A GitHub account.
Accounts for hosting services (like Heroku or Render).
A Pinecone API key (sign up at pinecone.io to get one).

Step-by-Step Setup Guide

Let’s get this app up and running from scratch. Follow these steps carefully:

1. Grab the Code
Open your terminal or command prompt.
Clone the project to your computer:

git clone https://github.com/ezhil2407/image-processing-app.git
cd image-processing-app
(Swap "your-username" with your actual GitHub username.)

2. Install Git (If You Don’t Have It)
If Git isn’t installed, download it from git-scm.com.
Check it worked - git --version

3. Install Python 3.10+ (If You Don’t Have It)
Head to python.org, download Python 3.10 or later and install it.
Make sure to tick "Add Python to PATH" during setup.
Verify it’s installed: python --version

Set Up Your Secret Key
Go to the backend folder: cd backend

Create a file called .env:
On Windows: type nul > .env then open it with Notepad.
On macOS/Linux: touch .env then edit with nano .env.
Add your Pinecone API key: PINECONE_API_KEY=your_pinecone_api_key_here   
Save and close the file.

5. Install the Tools
Go back to the root folder: cd ..

Install backend stuff: cd backend
pip install -r requirements.txt

Install frontend stuff: cd ../frontend
pip install -r requirements.txt

6. Double-Check Everything
Make sure no errors popped up while installing.
Confirm the .env file in the backend/ has your Pinecone key

Running the App
Here’s how to test it on your computer:

Start the Backend
Go to the backend folder: cd backend

Launch the FastAPI server: uvicorn main:app --reload

Open your browser and visit http://localhost:8000/. You should see a welcome message.

Start the Frontend
Open a new terminal tab and go to the frontend folder: cd frontend

Run the Streamlit app:streamlit run app.py

Frontend Deployment
Option 1: Streamlit Community Cloud
Push your code to GitHub (more on that later).
Visit share.streamlit.io, log in, and connect your repo.
Choose frontend/app.py.
Update the API URL in app.py to your backend’s live URL.
Deploy it and get a link (like https://your-username-image-processing.streamlit.app).

After Deployment
In frontend/app.py, change the requests.post URL to your backend’s live URL (e.g., https://image-processing-api.herokuapp.com/api/search).
Test it online to make sure everything works.

How to Use It
Open the frontend (http://localhost:8501/ locally or the deployed URL).
Text Search:
Pick the "Text" option.
Type something like "sunset beach".
Hit "Search".

Image Search:
Choose the "Image" option.
Upload a JPG, PNG, or JPEG file.
Click "Search".
See the Results:
Similar images will pop up below with their similarity scores.

License
This project uses the MIT License—check the LICENSE file for details.

Get in Touch
Author: Ezhilarasi
Email: ezhilkappu96@gmail.com
GitHub: ezhil2407



