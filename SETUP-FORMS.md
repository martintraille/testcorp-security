# Form Setup Instructions

Your website now supports file uploads for CV submissions and direct email delivery. To complete the setup, you need to create free Formspree accounts.

## Why Formspree?

- **Free tier**: 50 submissions per month
- **File uploads**: Supports CV/Resume attachments up to 10MB
- **Direct email**: Sends submissions directly to your email
- **No backend needed**: Works with static websites
- **Spam protection**: Built-in spam filtering
- **GDPR compliant**: Secure data handling

## Setup Instructions

### Step 1: Create Formspree Account

1. Go to [https://formspree.io/register](https://formspree.io/register)
2. Sign up with your email address (use careers@testcorpltd.com or admin@testcorpltd.com)
3. Verify your email address

### Step 2: Create Career Form

1. Log in to Formspree
2. Click **"New Form"**
3. Form name: `Career Applications`
4. Form email: `careers@testcorpltd.com`
5. Click **"Create Form"**
6. Copy the form endpoint URL (looks like: `https://formspree.io/f/xxxxxxxxx`)
7. Open `careers.html` in your editor
8. Find line 303: `action="https://formspree.io/f/YOUR_FORM_ID"`
9. Replace `YOUR_FORM_ID` with your actual form ID
   - Example: `action="https://formspree.io/f/mjkvqprl"`

### Step 3: Create Contact Form

1. In Formspree, click **"New Form"** again
2. Form name: `Contact Submissions`
3. Form email: `admin@testcorpltd.com`
4. Click **"Create Form"**
5. Copy the form endpoint URL
6. Open `index.html` in your editor
7. Find line 245: `action="https://formspree.io/f/YOUR_CONTACT_FORM_ID"`
8. Replace `YOUR_CONTACT_FORM_ID` with your actual form ID

### Step 4: Test Your Forms

1. Submit a test application on the careers page
2. First submission will require email confirmation (Formspree security feature)
3. Click the confirmation link in the email
4. Check that you receive the submission at careers@testcorpltd.com
5. Repeat for the contact form on the homepage

## Form Features

### Careers Form
- ✅ CV/Resume upload (PDF, DOC, DOCX - up to 10MB)
- ✅ All applicant information captured
- ✅ Sends to: careers@testcorpltd.com
- ✅ Subject: "New Career Application"

### Contact Form
- ✅ Service inquiry capture
- ✅ Project details
- ✅ Sends to: admin@testcorpltd.com
- ✅ Subject: "New Contact Form Submission"

## What You'll Receive

When someone submits a form, you'll receive an email with:
- All form field data formatted clearly
- CV/Resume attachment (careers form only)
- Applicant's email address (for easy reply)
- Timestamp of submission
- Option to download all data as CSV

## Formspree Dashboard Features

- View all submissions in your dashboard
- Export submissions as CSV
- Set up custom redirect pages
- Add custom validation rules
- Enable reCAPTCHA for extra spam protection
- View submission analytics

## Setting Up Custom Thank You Pages

To redirect users to professional thank you pages instead of Formspree's default page:

### For Career Applications Form:

1. Go to Formspree dashboard
2. Click on **"Career Applications"** form
3. Go to **"Settings"** tab
4. Find **"Redirect URL"** field
5. Enter the full URL to your thank you page:
   - If testing locally: `file:///path/to/thank-you-career.html`
   - Once hosted: `https://yoursite.com/thank-you-career.html`
6. Click **"Save"**

### For Contact Submissions Form:

1. Go to Formspree dashboard
2. Click on **"Contact Submissions"** form
3. Go to **"Settings"** tab
4. Find **"Redirect URL"** field
5. Enter the full URL:
   - If testing locally: `file:///path/to/thank-you-contact.html`
   - Once hosted: `https://yoursite.com/thank-you-contact.html`
6. Click **"Save"**

**Note:** The redirect will only work once your site is hosted with a proper domain. For local testing, you may still see the Formspree confirmation page.

## Alternative Services (if needed)

If you prefer not to use Formspree, here are alternatives:

1. **Web3Forms** (https://web3forms.com)
   - 250 submissions/month free
   - Similar setup process

2. **Netlify Forms** (if hosting on Netlify)
   - 100 submissions/month free
   - Integrated with Netlify hosting

3. **EmailJS** (https://www.emailjs.com)
   - 200 emails/month free
   - Client-side only

## Need Help?

If you need assistance with:
- Setting up the forms
- Customizing email templates
- Adding additional fields
- Implementing custom thank-you pages

Just let me know!

## Security Notes

- The `_gotcha` field is a honeypot for spam bots
- File uploads are scanned for viruses by Formspree
- All data is transmitted over HTTPS
- Formspree is GDPR compliant
- You can configure data retention policies in Formspree settings
