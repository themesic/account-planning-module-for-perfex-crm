# 🔧 Module Settings

Only **administrators** can access the Account Planning settings. Go to **Account Planning** → **Settings** (gear icon) to configure the module.

---

## Industry Options

**What it does:** Defines the list of industries you can assign to account plans (if your setup uses industry fields).

**How to set:**

- Enter one industry per line, or separate with commas.
- Example:
  ```
  Technology
  Healthcare
  Finance
  Retail
  ```

---

## Client Portal

**Enable client portal view for account plans**

- **On** – Clients can see their account plans in the client portal (read-only).
- **Off** – Clients cannot see account plans.

When enabled, clients see an **Account Planning** menu item and can view plans linked to their account. They can also request updates.

---

## Reminders

### Enable email reminders for planning tasks

- **On** – Staff assigned to plan tasks receive email reminders before the deadline.
- **Off** – No reminders are sent.

### Send reminders X days before task deadline

- Enter a number (e.g., **3**) to send reminders 3 days before the deadline.
- Default: 3 days.

**How it works:** The system creates Perfex reminders for tasks with a Person In Charge (PIC). When the cron job runs, it sends emails according to those reminders.

---

## Recurring Plan Periods

### Auto-create next period for completed plans

- **On** – The cron job will automatically copy completed plans to the next period (month or quarter).
- **Off** – No automatic copying.

### Period type

- **Monthly** – Copy on the 1st of each month.
- **Quarterly** – Copy on the 1st of January, April, July, October.

**How it works:**

- On the 1st of the month (or quarter), the cron checks for completed plans from the previous period.
- For each such plan, it creates a copy for the new period.
- It skips clients that already have a plan for the new period.

---

## Plan Status

### Default status for new plans

- **Draft** – New plans start as Draft.
- **In Progress** – New plans start as In Progress.
- **Review** – New plans start as Review.

Choose what makes sense for your workflow.

---

## Cron Job Setup

Reminders and recurring plans require the **Perfex cron job** to run regularly.

**Steps:**

1. Go to **Setup** → **Settings** → **Cron Job**.
2. Copy the cron URL or command shown.
3. Add it to your server's crontab to run daily (or as needed).

**Example (runs daily at 9:00 AM):**

```bash
0 9 * * * wget -q -O- https://yoursite.com/cron/index/YOUR_CRON_KEY
```

Replace `yoursite.com` and `YOUR_CRON_KEY` with your actual values.

---

## Webhooks

### What are webhooks?

Webhooks notify external systems when account plans are created, updated, or deleted. You provide a URL, and the module sends a POST request with JSON data when those events occur.

### Add webhook URL

1. Enter the full URL (e.g., `https://webhook.site/your-id` or your own endpoint).
2. Click **Add**.
3. The URL is saved. All plan create/update/delete events will be sent there.

### Webhook options

**Disable SSL verification for webhooks**

- **On** – Skips SSL certificate verification (useful for testing with services like webhook.site).
- **Off** – Normal SSL verification (recommended for production).

---

## Next Steps

- [Client Portal](client-portal/client-portal.md)
- [Troubleshooting](troubleshooting/troubleshooting.md)
