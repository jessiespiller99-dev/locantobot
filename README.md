# 🤖 Locanto Automation Bot

A powerful automation system for creating accounts and posting on Locanto.com.au using mail.com alias emails.

## ✨ Features

- **🔐 Automated Account Creation**: Creates Locanto accounts using mail.com alias emails
- **📧 Email Management**: Automatically creates 9 alias emails from your mail.com account
- **✅ Email Verification**: Automatically checks inbox and verifies accounts
- **📮 Automated Posting**: Creates 5 posts per account using your templates
- **📊 Beautiful Dashboard**: Modern, responsive UI to manage everything
- **📝 Template Management**: Import templates from Excel/CSV or add manually
- **👥 Account Tracking**: View all created accounts and their status
- **📋 Activity Logs**: Monitor all automation activities
- **🗑️ Data Management**: Clear data selectively or all at once

## 🚀 Getting Started

### Prerequisites

- Node.js 20+ or Bun
- Chrome browser (for automation)
- A mail.com account

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd locanto-automation
```

2. Install dependencies:
```bash
bun install
```

3. Start the development server:
```bash
bun dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## 📖 How to Use

### Step 1: Prepare Templates

1. Go to the **Templates** tab
2. Either:
   - **Import from Excel**: Upload an Excel/CSV file with columns: `title`, `description`, `city`, `category`
   - **Add Manually**: Fill in the form and click "Add Template"

### Step 2: Start Automation

1. Go to the **Automation** tab
2. Enter your mail.com credentials:
   - Email: your-email@mail.com
   - Password: your password
3. Set the number of accounts to create (1-9)
4. Click **Start Automation**

### What Happens Next:

1. ✅ Logs into your mail.com account
2. ✅ Creates 9 alias email addresses
3. ✅ Registers Locanto accounts with female names (auto-generated)
4. ✅ Checks mail.com inbox for verification emails
5. ✅ Opens verification links in your PC browser
6. ✅ Updates profile settings (date of birth, etc.)
7. ✅ Creates 5 posts per account using your templates
8. ✅ Tracks everything in the dashboard

### Step 3: Monitor Progress

- **Dashboard**: View statistics and system overview
- **Accounts**: See all created accounts and their status
- **Posts**: View all created posts
- **Logs**: Monitor automation activity

## 📂 Excel Template Format

Your Excel file should have these columns:

| title | description | city | category |
|-------|-------------|------|----------|
| Looking for fun | Hi, I'm looking for a good time... | Sydney | men-looking-for-men |
| Available tonight | Professional escort available... | Melbourne | escorts |

**Categories:**
- `men-looking-for-men` - Personals > Casual Encounters > Men Looking for Men
- `escorts` - Personals > Services > Escorts

## 🛠️ Tech Stack

- **Frontend**: Next.js 16, React 19, TypeScript, Tailwind CSS 4
- **Backend**: Next.js API Routes
- **Database**: SQLite with Drizzle ORM
- **Automation**: Puppeteer with Stealth Plugin
- **Excel Import**: XLSX library

## 📁 Project Structure

```
├── src/
│   ├── app/                    # Next.js app directory
│   │   ├── api/                # API routes
│   │   │   ├── automation/     # Automation endpoints
│   │   │   ├── templates/      # Template management
│   │   │   ├── stats/          # Statistics
│   │   │   └── clear/          # Data clearing
│   │   ├── page.tsx            # Main dashboard page
│   │   └── layout.tsx          # Root layout
│   ├── components/             # React components
│   │   ├── Dashboard.tsx       # Main dashboard
│   │   ├── AutomationControl.tsx
│   │   ├── TemplateManager.tsx
│   │   ├── AccountsView.tsx
│   │   ├── PostsView.tsx
│   │   └── LogsView.tsx
│   ├── db/                     # Database
│   │   ├── schema.ts           # Database schema
│   │   └── index.ts            # Database connection
│   └── lib/                    # Utilities
│       ├── automation/         # Automation modules
│       │   ├── mail-com.ts     # Mail.com automation
│       │   └── locanto.ts      # Locanto automation
│       ├── browser.ts          # Browser utilities
│       └── utils.ts            # Helper functions
└── data/                       # SQLite database (auto-created)
```

## ⚠️ Important Notes

1. **Browser Automation**: The automation runs in a visible Chrome browser so you can see what's happening
2. **Rate Limiting**: The system includes random delays to avoid detection
3. **Email Verification**: Make sure your mail.com account can receive emails
4. **Templates**: You need to add templates before running automation
5. **Categories**: Only two categories are supported as per requirements

## 🔒 Security

- Never commit your mail.com credentials
- The database is stored locally in the `data/` directory
- All automation happens on your local machine

## 🐛 Troubleshooting

### Automation fails to start
- Check your mail.com credentials
- Ensure Chrome is installed
- Check if mail.com or locanto.com websites have changed their structure

### Email verification not working
- Wait a few minutes for emails to arrive
- Check your mail.com inbox manually
- Ensure your mail.com account is not blocked

### Templates not importing
- Check Excel file format (columns: title, description, city, category)
- Ensure all required fields are filled
- Try CSV format if Excel doesn't work

## 📝 License

This project is for educational purposes only. Use responsibly and in accordance with the terms of service of mail.com and locanto.com.au.

## 🤝 Support

For issues or questions, please check the logs in the dashboard or review the browser automation process.
