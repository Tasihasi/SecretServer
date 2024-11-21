# Secret Management React App

This is a simple React app built with TypeScript that allows users to store a secret text and retrieve it later using a unique hash. The app provides two main features:

**Save Secret:** Allows users to store a secret, specify how many times it can be retrieved, and set an expiry time for the secret.

**Retrieve Secret:** Allows users to retrieve a previously stored secret using its unique hash.
 
The app interacts with a backend API to store and retrieve secrets.

### The backend GitHub Repo: https://github.com/Tasihasi/SecretServerBackEnd

# Features

## Save Secret:

Users can input a secret text.

Users can set the number of times the secret can be retrieved.

Users can set the expiry date for the secret (in minutes).

After submission, the app generates a unique hash that can be used to retrieve the secret.

The hash is copied to the clipboard with one click for easy sharing.

## Retrieve Secret:

Users can input a hash to retrieve the corresponding secret text.

If the hash is valid and the secret has not expired, the secret is displayed.

In case of errors (invalid hash or expired secret), the app shows an appropriate error message.

# How It Works 

## Save Secret

When a user enters the secret text, the number of retrievals allowed, and the expiry date (in minutes), the data is sent to the backend via a POST request. If the submission is successful, the server returns a unique hash that the user can use to retrieve the secret. The hash is displayed and can be copied to the clipboard.

## Retrieve Secret

To retrieve a secret, the user enters the hash in the corresponding field and submits the form. A GET request is made to the backend with the hash to fetch the secret. If the hash is valid and the secret has not expired, it will be displayed on the screen. Otherwise, an error message is shown.

# Technologies Used

**React** JavaScript library for building user interfaces.
**TypeScript** A typed superset of JavaScript that provides type safety and improves development experience.
**CSS** For styling the components (you can customize styles according to your preference).

# Backend

This app requires a **backend server** and **database** to handle secret storage and retrieval.  

### The backend GitHub Repo: https://github.com/Tasihasi/SecretServerBackEnd

The backend API endpoints used are:

    POST /secret: To save a new secret.
    GET /secret/{hash}: To retrieve the secret using its hash.

Make sure the backend is running and properly configured before using the app.

