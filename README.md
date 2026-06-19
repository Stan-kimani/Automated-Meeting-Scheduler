# Automated Meeting Scheduler

An n8n workflow that automates meeting scheduling - from email request to calendar booking.

![n8n](https://img.shields.io/badge/n8n-Automation-blue)
![Google Calendar](https://img.shields.io/badge/Google_Calendar-Integration-green)
![Gmail](https://img.shields.io/badge/Gmail-API-red)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## What It Does

1. Listens for "schedule a meeting" emails
2. Checks your Google Calendar for free slots
3. Sends 3 available time options
4. Books the meeting when you reply "CONFIRM 1/2/3"
5. Creates Google Calendar event with Google Meet link

---

##  Features

-  Automatic email parsing (sender, topic, duration)
- Real-time calendar availability check
-  Interactive email responses with time slots
-  One-click confirmation (CONFIRM 1/2/3)
-  Auto-creates calendar events with Google Meet
-  Slack notifications for booked meetings

---

## Installation

### 1. Import the Workflow
- Go to n8n → Workflows → Import from File
- Upload `Automated Meeting Scheduler.json`

### 2. Add Credentials
| Service | Required |
|---------|----------|
| Gmail OAuth2 | Yes |
| Google Calendar OAuth2 | Yes |
| Slack Webhook |  Optional |

### 3. Update Timezone
Change `Africa/Nairobi` to your timezone in:
- `Extract Meeting Details` node
- `Find Free Slots` node

### 4. Activate
Click the **Active** toggle and send a test email!

---

## How to Use

### For Meeting Requesters:
1. Send email with "schedule a meeting" in subject
2. Receive 3 time slot options
3. Reply: `CONFIRM 1`, `CONFIRM 2`, or `CONFIRM 3`
4. Get confirmation with Google Meet link


---

## Technologies Used

- **n8n** - Workflow automation
- **Gmail API** - Email handling
- **Google Calendar API** - Availability & booking
- **Slack API** - Team notifications
- **JavaScript** - Custom logic nodes

---


---

## Configuration Options

| Setting | Default | Where to Change |
|---------|---------|-----------------|
| Working Hours | 9 AM - 5 PM | `Find Free Slots` node |
| Business Days | 3 days | `Build Date Ranges` node |
| Default Duration | 30 minutes | `Extract Meeting Details` node |
| Timezone | Africa/Nairobi | Multiple nodes |

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Could not find sender" | Check Gmail Trigger version |
| No slots found | Adjust working hours in `Find Free Slots` |
| Confirmation not parsed | Reply exactly with "CONFIRM 1/2/3" |
| Calendar not creating | Verify Google Calendar permissions |

---

## Contributing

1. Fork the workflow
2. Make your changes
3. Submit a pull request

---

## License

MIT License - see [LICENSE](LICENSE) file for details

---

## Contact

**Your Name** – [@yourtwitter](https://twitter.com/yourtwitter) – email@example.com

Project Link: [https://github.com/yourusername/automated-meeting-scheduler](https://github.com/yourusername/automated-meeting-scheduler)

---

## Quick Start

1. Import workflow to n8n
2. Add Gmail & Calendar credentials
3. Update timezone
4. Activate workflow
5. Send test email: "Schedule a meeting"

**That's it! Your automated scheduler is live!** 

---

*Built using n8n*

