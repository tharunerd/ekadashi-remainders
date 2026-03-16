# 🌙 Ekadashi Reminders

Automated email alerts the day before every Ekadashi — powered by GitHub Actions

***

## 📌 About This Project

This is a very simple personal automation project.

I (Tharun) wanted to get an **email reminder one day before every Ekadashi**, so I created a GitHub Actions workflow that sends myself an email automatically on specific dates.

No complex code, no heavy setup — just a list of Ekadashi dates + GitHub’s built‑in scheduler.

***

## ✨ What It Does

*   Sends me an email reminder **one day before Ekadashi**
*   Runs completely automatically using **GitHub Actions**
*   Uses simple **cron schedules** matching each Ekadashi date
*   Sends email through SMTP (Gmail App Password)

That’s it. Super minimal.

***

## 🛕 Why I Built This

I kept forgetting Ekadashi 😅  
So instead of depending on calendar apps or reminders, I made GitHub do it for me.

GitHub Actions runs every day anyway — might as well put it to spiritual use.

***

## 📅 How It Works

Inside `.github/workflows/ekadashi-reminders.yml`:

*   Each Ekadashi date is converted to a **cron expression**
*   GitHub runs the workflow at **7:00 AM IST** the day before
*   It sends an email to me (and optional multiple recipients)
*   All credentials like email/password are stored safely in **GitHub Secrets**

***

## 📧 Email Setup

The workflow uses `dawidd6/action-send-mail` to send the reminder email.  
I just added these as repository secrets:

| Secret                            | Purpose                            |
| --------------------------------- | ---------------------------------- |
| `EMAIL_SERVER`                    | SMTP server (e.g., smtp.gmail.com) |
| `EMAIL_PORT`                      | 465 (SSL)                          |
| `EMAIL_USERNAME`                  | My Gmail address                   |
| `EMAIL_PASSWORD`                  | Gmail App Password (16 chars)      |
| `RECIPIENT_EMAIL` OR `RECIPIENTS` | One or multiple email IDs          |

***

## ⚙️ How to Use (if someone else wants it)

1.  Fork this repo
2.  Add your own Ekadashi dates inside the workflow file
3.  Add your Gmail credentials in repo secrets
4.  Commit & push
5.  GitHub will start emailing you automatically

***

## 🕉️ Example Email Body

    Namaste!  
    Tomorrow is Ekadashi.

    A good day for fasting, devotion, and reflection.

    Hari Om 🙏

***

## ✔️ Status

Fully automated.  
Zero maintenance.  
Runs by itself every month.

***

## 💛 Credits

Made by me for myself — but open for anyone who finds it useful.

***
