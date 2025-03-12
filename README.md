# Google Forms Slack Notification Template

[English](README.md) | [한국어](README.ko.md) | [Español](README.es.md)

A template management tool for automatically sending Slack notifications when receiving Google Form responses in Google Sheets.

## Features

- Automatically sends Slack notifications when Google Forms are submitted
- Manages various notification templates (add, edit, duplicate, delete)
- Set active templates to use your preferred notification format
- Easily use form fields as template variables
- Template preview and testing functionality

## Installation

1. Open your Google Spreadsheet.
2. Select `Extensions` > `Apps Script` from the top menu.
3. When the Apps Script editor opens, delete all existing code and paste the contents of the `Code.gs` file from this repository.
4. In the file menu, click `+ New file` and select `HTML` file.
5. Name the file `Sidebar` and paste the contents of the `Sidebar.html` file from this repository.
6. Click the save button.
7. When you return to the spreadsheet, a `Slack Notification Settings` menu will be created at the top.

## How to Use

1. Set up an Incoming Webhook in Slack. ([How to set up Slack webhooks](https://api.slack.com/messaging/webhooks))
2. In the spreadsheet, click `Slack Notification Settings` > `Open Sidebar`.
3. Enter the webhook URL you received from Slack in the webhook URL settings section and save it.
4. Click the 'Add New Template' button in the template management section to create a template.
5. You can use variables in the template content in the format `{{field_name}}`.
6. Click on the desired template to set it as the active template.
7. Click the Form Submission Trigger Setup button to activate automatic notifications.

## Template Examples

```
Name: {{name}}
Phone: {{phone}}
Reason: {{reason}}
```

```
{{name}}({{phone}})
{{reason}}
```

```
({{people_count}} people){{name}}
{{phone}}
{{reason}}
```
