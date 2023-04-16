## Emailer-2.0
Emailer-2.0 is a fork of J-Calder/Emailer-2.0, a Python-based application that allows you to send personalized emails to multiple recipients using a CSV file and a template.

## Features
- Send emails with attachments and inline images
- Use Jinja2 syntax to customize your email template with variables from the CSV file
- Use SMTP or Gmail as your email provider
- Use environment variables or a config file to store your credentials and settings
- Use logging and error handling to monitor your email campaign

## Requirements
- Python 3.6 or later
- Pipenv
= A CSV file with your recipients’ information
- An HTML file with your email template
- An email account with SMTP or Gmail access

## Installation
To install Emailer-2.0, follow these steps:

- Clone this repository: git clone https://github.com/rasteia/Emailer-2.0.git
- Change directory to the project folder: cd Emailer-2.0
- Install the dependencies using Pipenv: pipenv install
- Activate the virtual environment: pipenv shell

## Usage
To use Emailer-2.0, follow these steps:

- Create a CSV file with your recipients’ information, such as name, email, etc. The first row should contain the column names.
- Create an HTML file with your email template, using Jinja2 syntax to insert variables from the CSV file, such as {{name}}, {{email}}, etc.
- Create a folder named “attachments” and place any files you want to attach to your emails inside it.
- Create a folder named “images” and place any images you want to embed in your emails inside it. Use the cid: prefix to reference them in your HTML file, such as <img src="cid:image.jpg">.
- Set up your credentials and settings using one of these methods:
- Environment variables: Set the following variables in your system or in a .env file in the project folder:
- EMAIL_USER: Your email username
- EMAIL_PASS: Your email password
- EMAIL_PROVIDER: Your email provider (SMTP or Gmail)
- EMAIL_HOST: Your email host (only for SMTP)
- EMAIL_PORT: Your email port (only for SMTP)
- EMAIL_FROM: Your email address
- EMAIL_SUBJECT: Your email subject
- EMAIL_CSV: The name of your CSV file
- EMAIL_HTML: The name of your HTML file
- Config file: Create a config.json file in the project folder with the following structure:
```
{
  "user": "your email username",
  "pass": "your email password",
  "provider": "your email provider (SMTP or Gmail)",
  "host": "your email host (only for SMTP)",
  "port": "your email port (only for SMTP)",
  "from": "your email address",
  "subject": "your email subject",
  "csv": "the name of your CSV file",
  "html": "the name of your HTML file"
}
```

# Run the main.py script: python main.py
Check the logs.txt file for any errors or warnings.

License
This project is licensed under the MIT License - see the LICENSE file for details.
