# Pricing Service

This is an application built to allow the periodic scanning of online webstores, to notify users of changes in prices of items they select.

This application is part of the course "The Complete Python Web Developer", a course aimed at beginners, to teach the creation of web applications using Python. If that sounds interesting, check it out: https://www.udemy.com/the-complete-python-web-course-learn-by-building-8-apps/

It allows administrators (defined via `src/config.py`) to add, remove, and edit online stores.

You will need a Mailgun account and API details for the e-mailing to work.
E-mails are sent via executing the `src/alert_updater.py` file. In order to check e.g. every 10 minutes, the file must be executed every 10 minutes. This can be done with a cron job or a Windows service.
Mailgun seems to have stoped working... not yet fixed.

It parses the store websites using `requests` and `BeautifulSoup`.

It **does not work with Stores that dynamically inject content using JavaScript**.

It allows users to register, log in, and create and modify their alerts.

Technology stack: MongoDB, Python (Flask & Jinja2), HTML/CSS/Bootstrap, Mailgun.

You can access the website at https://discount-tracker-website-edlgg.herokuapp.com
you can create a user or use the following:
admin@admin.com 123
test@test.com 123


![Home Screen](readme-files/home.png)

![Sign up Screen](readme-files/signup.png)

![Alerts Screen](readme-files/alerts.png)

![Create Alert Screen](readme-files/create_alert.png)

![Stores Screen](readme-files/stores.png)

![Edit Store Screen](readme-files/edit_store.png)