🎢 Theme Park Flask PWA Workbook (GitHub Codespaces)

This workbook guides students through setting up and developing the Theme Park Progressive Web App (PWA) using Flask inside GitHub Codespaces. By working in Codespaces, students don’t need to install Python or Flask locally — everything runs in the cloud.

Part A: Introduction

What is GitHub Codespaces?

Cloud-based dev environment: Runs VS Code in the browser.

No local setup needed: Python, Flask, and extensions are pre-installed.

Reproducible: Same environment for every student.

Why use Codespaces for the Theme Park PWA?

Accessibility: Works on school computers, Chromebooks, or tablets.

Consistency: Everyone has the same Python version and dependencies.

Collaboration: Code is stored on GitHub, easy to share and review.

Part B: Setting Up the Project

Step 1: Fork the Repository

Go to the Theme Park PWA GitHub repository (teacher provides link).

Click Fork to create your own copy.

Step 2: Open in Codespaces

On your forked repo, click the green Code button.

Select Open with Codespaces → New Codespace.

Wait for VS Code in the browser to load.

Step 3: Verify Environment

Open the terminal in Codespaces.

Run:

python --version
pip --version

Confirm Python 3.x and pip are available.

Part C: Installing Dependencies

Step 1: Requirements File

The repo includes requirements.txt.

Install dependencies:

pip install -r requirements.txt

Step 2: Verify Flask

Run:

python -m flask --version

Confirm Flask is installed.

Part D: Running the Flask App

Step 1: Start the App

flask run --host=0.0.0.0 --port=5000

Step 2: Preview in Browser

Codespaces shows a Port 5000 notification.

Click Open in Browser.

You should see the Theme Park PWA homepage.

Part E: Project Structure

/themepark-pwa
│
├── app.py              # Main Flask app
├── static/             # CSS, JS, images
├── templates/          # HTML templates (Jinja2)
├── requirements.txt    # Dependencies
├── Procfile            # Deployment config (Heroku/Render)
└── README.md           # Project instructions

Key Files

app.py: Defines routes and logic.

templates/: Contains index.html, booking.html, etc.

static/: Holds CSS, JS, and images.

requirements.txt: Lists pinned versions.

Part F: Developing Features

Example: Adding a New Ride Page

Create templates/ride.html.

Add route in app.py:

@app.route("/ride")
def ride():
    return render_template("ride.html")

Restart Flask and preview.

Example: Updating Navigation

Edit templates/base.html.

Add link:

<a href="/ride">New Ride</a>

Part G: Saving & Committing

Step 1: Stage Changes

git add .

Step 2: Commit Changes

git commit -m "Added new ride page"

Step 3: Push to GitHub

git push origin main

Part H: Deployment (Optional)

Step 1: Prepare Procfile

web: flask run --host=0.0.0.0 --port=$PORT

Step 2: Deploy to Heroku/Render

Connect GitHub repo.

Enable auto-deploy.

Visit live Theme Park PWA URL.

Part I: Reflection Questions

Why is Codespaces useful for classroom projects?

How does Flask separate logic (app.py) from presentation (templates/)?

What are the benefits of pinned versions in requirements.txt?

How does GitHub help with collaboration?

Part J: Extension Challenge

Add a booking form with WTForms.

Store bookings in a SQLite database.

Display all bookings on an admin page.

This workbook ensures students can set up, run, and extend the Theme Park Flask PWA entirely in GitHub Codespaces, without needing a local environment.