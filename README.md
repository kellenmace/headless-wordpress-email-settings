# Headless WordPress Email Settings

This is a WordPress plugin that customizes email settings to work well with a decoupled frontend application.

It does this:

- Changes the "from" address for emails from `wordpress@domain.com` to `info@domain.com`.
- Changes the "from" name for emails from `WordPress` to the title of your WordPress site. You can set this in `Settings` > `General` > `Site Title` in the WordPress admin.
- Changes the password reset email subject line from `[My Site Title] Password Reset` to `My Site Title - Password Reset`, where "My Site Name" is the title of your WordPress site.
- Customizes the password reset email message and modifies the password reset link to point to your decoupled frontend JS app.
- Customizes the new user notification email subject and message, and modifies the set password link to point to your decoupled frontend JS app.

## How to Use

1. Define a `FRONTEND_APP_URL` constant in your project (usually in `wp-config.php`) that points to the URL of your decoupled frontend JS app. Alternatively, you can modify line `86` of the plugin to get the frontend app URL some other way (hardcode it, get it from the database, etc.).
1. Modify the email from address, password reset subject, password reset message and new user notification email subject & message text, if desired.
1. Install and activate the plugin.
1. Test the password reset and new user sign up flows in your frontend JS app and review the emails that WordPress sends out.

## Screenshots

### Password Reset Email

<img width="1772" alt="Screenshot of password reset email" src="https://user-images.githubusercontent.com/5306336/123113272-6be81500-d40c-11eb-9799-e73c0a5bbfe6.png">

### New User Sign Up Email

<img width="1772" alt="Screenshot of new user sign up email" src="https://user-images.githubusercontent.com/5306336/123113382-83bf9900-d40c-11eb-9cad-cef3e2d0ce7d.png">
