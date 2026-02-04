# Troubleshooting

This page covers common issues and solutions for the Account Planning module.

---

## Module Not Showing / Not Active

**Symptom:** Account Planning does not appear in the menu, or it shows as inactive.

**Solutions:**

1. **Activate the module** – Go to Setup → Modules, find Account Planning, and activate it with your purchase code.
2. **Check permissions** – Ensure your staff role has at least **View** permission for Account Planning.
3. **Clear cache** – Clear your browser cache and reload the page.
4. **Verify installation** – Re-upload the module ZIP if the files are missing or corrupted.

---

## 419 Page Expired When Submitting Forms

**Symptom:** When you submit a form (e.g., meeting note, competitor), you get "419 Page Expired" or similar.

**Cause:** CSRF (security) token mismatch—often because the page was open too long or the session expired.

**Solutions:**

1. **Refresh the page** and try again.
2. **Log out and log back in**, then retry.
3. Ensure your **session timeout** in Perfex is not too short (Setup → Settings → General).
4. Do not open the same form in multiple tabs.

---

## Reminders Not Sending

**Symptom:** Staff do not receive email reminders for plan tasks.

**Solutions:**

1. **Enable reminders** – Settings → Account Planning → Enable email reminders.
2. **Set reminder days** – e.g., 3 days before deadline.
3. **Configure cron** – The cron job must run regularly. Go to Setup → Settings → Cron Job and add the URL to your server's crontab.
4. **Check task assignee** – Tasks must have a Person In Charge (PIC) to receive reminders.
5. **Check Perfex email** – Ensure Perfex can send emails (Setup → Settings → Email).

---

## Recurring Plans Not Auto-Creating

**Symptom:** Completed plans are not copied to the next period automatically.

**Solutions:**

1. **Enable recurring** – Settings → Account Planning → Auto-create next period for completed plans.
2. **Configure cron** – Same as reminders; the cron must run (e.g., daily).
3. **Check date** – Monthly runs on the 1st; quarterly runs on 1st of Jan, Apr, Jul, Oct.
4. **Check plan status** – Only **Completed** plans are copied.
5. **Check for duplicates** – The system skips clients that already have a plan for the new period.

---

## Client Portal Not Showing Plans

**Symptom:** Clients log in but do not see Account Planning or any plans.

**Solutions:**

1. **Enable client portal** – Settings → Account Planning → Enable client portal view.
2. **Check client** – Ensure the plan is linked to the correct client.
3. **Check plan status** – Some setups may hide draft plans from clients; verify which statuses are visible.
4. **Client login** – Ensure the client is logging in with the correct account.

---

## Unserialize Error on Project View

**Symptom:** When opening a project created via Quick Create Project, you see an "unserialize()" error.

**Cause:** Older versions stored project settings incorrectly. This has been fixed in module updates.

**Solutions:**

1. **Update the module** to the latest version (includes a migration fix).
2. If the error persists, contact support—a database fix may be needed for existing projects.

---

## MindMap / TinyMCE Not Loading

**Symptom:** The MindMap or rich text editor does not appear or shows a blank area.

**Solutions:**

1. **Refresh the page** – Sometimes assets load slowly.
2. **Check browser console** – Look for JavaScript errors (F12 → Console).
3. **Disable browser extensions** – Ad blockers or script blockers can interfere.
4. **Try another browser** – Rule out browser-specific issues.
5. **Check file permissions** – Ensure the `modules/accountplanning/assets` folder is readable by the web server.

---

## Webhooks Not Firing

**Symptom:** Your webhook URL is added but no requests are received.

**Solutions:**

1. **Test the URL** – Use a service like webhook.site to verify the URL works.
2. **SSL verification** – If using a self-signed or test URL, enable "Disable SSL verification" in Settings.
3. **Firewall** – Ensure your server can make outbound HTTP requests to the webhook URL.
4. **Check events** – Webhooks fire on plan create, update, and delete. Create or edit a plan to test.

---

## Export PDF / Excel Fails

**Symptom:** Export button does nothing or shows an error.

**Solutions:**

1. **Check permissions** – You need View permission.
2. **Large data** – Very large plans or tables may timeout; try filtering to fewer plans.
3. **Browser** – Try a different browser or disable pop-up blockers for the export.
4. **Server** – Check PHP memory limit and max execution time if exports fail on large datasets.

---

## Custom Fields Not Showing

**Symptom:** Custom fields configured for Account Planning do not appear.

**Solutions:**

1. **Create custom fields** – Setup → Custom Fields → Add field for **Account Planning** type.
2. **Clear cache** – Refresh the page after adding fields.
3. **Check form** – Custom fields appear on the new account form and possibly in the plan view.

---

## Need More Help?

- Review the [Settings](settings/settings.md) for configuration options.
- Check that your [Perfex CRM version](README.md#requirements) is 2.3 or higher.
- Contact the module author or CodeCanyon support for license or technical issues.
