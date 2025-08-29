# Community Forum Setup Guide

Welcome to your new forum! This guide will walk you through the entire process of setting up the backend, customizing the code, and deploying it online so you can embed it in your Wix website. No coding experience is needed, just follow these steps carefully.

## Part 1: Setting Up Your Firebase Backend

Firebase is a service from Google that will act as the "brain" for your forum. It will handle user accounts, store all the posts and comments, and keep everything secure.

### Step 1: Create a Firebase Project

1. Go to the [Firebase Console](https://console.firebase.google.com/). You'll need to sign in with a Google account.
2. Click on **"Add project"**.
3. Give your project a name (e.g., "my-wix-forum") and click **Continue**.
4. You can disable Google Analytics for this project if you want. Click **"Create project"**. Wait for it to finish.

### Step 2: Set Up a Web App in Firebase

1. Once your project is ready, you'll be on the project dashboard. Click the **Web icon** (it looks like `</>`).
2. Give your app a nickname (e.g., "Forum App") and click **"Register app"**.
3. Firebase will now show you your `firebaseConfig` object. This is very important! **Copy this entire block of code**.
4. Open the `index.html` file on your computer. Find the section that says `// --- START: PASTE YOUR FIREBASE CONFIG HERE ---`. **Paste your copied config object there**, replacing the placeholder one.
5. After pasting, you can click **"Continue to console"** in Firebase.

### Step 3: Enable Authentication

1. In the Firebase console, go to the **"Build"** menu on the left and click **"Authentication"**.
2. Click the **"Get started"** button.
3. In the "Sign-in method" tab, click on **"Email/Password"**.
4. **Enable** the toggle switch and click **"Save"**.

### Step 4: Create Your Firestore Database

1. In the Firebase console, go to the **"Build"** menu on the left and click **"Firestore Database"**.
2. Click **"Create database"**.
3. Choose to start in **Production mode**. Click **Next**.
4. Choose a location for your database and click **"Enable"**.

### Step 5: Set Up Security Rules

1. In your Firestore Database screen, click on the **"Rules"** tab at the top.
2. Delete everything in the text box and **replace it with the following rules**:
