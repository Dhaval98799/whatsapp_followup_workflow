# 💬 WhatsApp Follow-up Automation

> **n8n automation** — Sends WhatsApp follow-up messages to buyers from Google Sheet using WhatsApp Business API or Twilio.

---

## What This Does

```
Google Sheet → Check due follow-ups → Send WhatsApp message → Update Sheet
```

---

## Features

- ✅ Reads buyer phone numbers from Google Sheet
- ✅ AI writes personalized WhatsApp message
- ✅ Sends via WhatsApp Business API (Meta) or Twilio
- ✅ Tracks message status: Sent / Delivered / Read
- ✅ 3-message follow-up sequence with delays
- ✅ Runs daily at 10 AM

---

## WhatsApp API Options

| Option | Cost | Setup |
|--------|------|-------|
| **Meta WhatsApp Business API** | Free (up to 1000/month) | Medium |
| **Twilio WhatsApp** | $0.005/message | Easy |
| **WATI** | $49/month | Easy |

---

## Message Templates

**Message 1 (Day 1):**
```
Hello [Name]! 👋
This is [Your Name] from [Company].
We export [Product] to [Country].
Would you like our product catalog?
```

**Message 2 (Day 4):**
```
Hi [Name], following up on my earlier message.
Our [Product] is available for immediate shipment.
Interested in a price quote?
```

**Message 3 (Day 8 - Final):**
```
Hello [Name], last follow-up from my side.
If you need [Product] anytime, please reach out.
Best regards, [Your Name]
```

---

## Google Sheet Columns

```
A: WA_Status          (Pending / Sent / Completed / Stop)
B: Row_Number
C: Buyer_Name
D: Company_Name
E: Country
F: Phone_Number       (+91XXXXXXXXXX format)
G: Product_Interest
H: WA_Count           (0, 1, 2)
I: Next_WA_Date
J: Last_WA_At
K: Notes
```

---

## Setup

### Replace in Workflow

| Placeholder | Replace With |
|------------|-------------|
| `YOUR_SHEET_ID` | Google Sheet ID |
| `YOUR_TWILIO_SID` | Twilio Account SID |
| `YOUR_TWILIO_TOKEN` | Twilio Auth Token |
| `YOUR_WA_NUMBER` | Your WhatsApp number (+1415XXXXXXX) |
| `YOUR_GROQ_KEY` | Groq free API key |
| `YOUR_COMPANY_NAME` | Your company |
| `YOUR_PRODUCT` | Your export product |
