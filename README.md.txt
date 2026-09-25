# Phishing Website Simulation

## Overview

This project is a **Flask-based phishing simulation web application** developed for educational and cybersecurity awareness purposes. The application demonstrates the technical workflow of a credential-phishing attack by presenting a simulated login interface, processing submitted form data on a Python backend, and forwarding the captured test data to a configured Discord webhook.

The project demonstrates the interaction between a **frontend HTML interface**, a **Flask web server**, HTTP form submission, server-side request handling, and an external webhook-based notification mechanism.

## Technologies Used

* **Python** – Backend application logic
* **Flask** – Lightweight Python web framework used to create the web server and handle HTTP requests
* **HTML** – Frontend structure and simulated login interface
* **Requests** – Python HTTP library used for communication with the external webhook endpoint
* **Discord Webhooks** – Used as the notification/communication endpoint for the controlled demonstration

## Technical Workflow

The application follows a simple client-server architecture:

1. A user accesses the Flask application through a web browser.
2. Flask renders the HTML-based simulated login page.
3. The user submits the login form through an HTTP request.
4. Flask receives the submitted form data using the `request` object.
5. The backend processes the received data.
6. The Python `requests` library is used to send the demonstration data to the configured webhook endpoint.
7. The server returns an appropriate response to the browser using Flask's response-handling functionality.

## Backend Components

The Python backend uses Flask to provide the application's HTTP interface.

```python
from flask import Flask, render_template, request, jsonify
import requests
```

* `Flask` initializes the web application.
* `render_template` serves the HTML frontend.
* `request` provides access to incoming HTTP form data.
* `jsonify` can be used to return structured JSON responses.
* `requests` handles outbound HTTP communication with the configured webhook.

## Frontend

The frontend is implemented using HTML and represents a simulated authentication page. Its purpose is to demonstrate how visually convincing login interfaces can be used in phishing attacks and why users should verify the authenticity of websites before entering credentials.

## Security Demonstration

The project demonstrates several concepts relevant to web security:

* Social engineering through simulated login pages
* HTTP form submission
* Client-server communication
* Server-side request processing
* External HTTP API/webhook communication
* Credential-phishing attack flow
* Security awareness and phishing detection

## Educational Scope

This application is designed for use in a **controlled laboratory or academic environment**. Only dummy credentials and test data should be used during demonstrations. The project should not be deployed to collect real users' credentials or used to impersonate real organizations or services without explicit authorization.

## Disclaimer

This project is intended exclusively for **authorized cybersecurity education, research, and awareness demonstrations**. Any collection or transmission of real credentials without authorization is prohibited. The author assumes no responsibility for misuse of the project.
