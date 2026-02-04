# Permissions

The Account Planning module uses Perfex CRM's permission system. You control who can view, create, edit, and delete account plans.

---

## Why Permissions Matter

- **Security** – Only authorized staff can see or change account plans.
- **Workflow** – Some users may only need to view plans; others need to create and edit them.
- **Compliance** – Sensitive client data stays restricted to the right people.

---

## Available Permissions

| Permission | What It Allows |
|------------|----------------|
| **View** | See the Account Planning menu, list of plans, and plan details |
| **Create** | Create new account plans, use templates, add relations |
| **Edit** | Modify existing plans, update tasks, change status |
| **Delete** | Delete account plans and related data |

---

## How to Assign Permissions

1. Go to **Setup** → **Staff** (or **Setup** → **Roles**).
2. Select the **staff member** or **role** you want to configure.
3. Find the **Account Planning** section in the permissions list.
4. Check the boxes for the permissions you want to grant:
   - **View** (Global)
   - **Create**
   - **Edit**
   - **Delete**
5. Save your changes.

---

## Recommended Setups

### Account Manager (full access)

- View: Yes  
- Create: Yes  
- Edit: Yes  
- Delete: Yes  

### Sales Representative (create and edit only)

- View: Yes  
- Create: Yes  
- Edit: Yes  
- Delete: No  

### Read-Only (e.g., executives)

- View: Yes  
- Create: No  
- Edit: No  
- Delete: No  

---

## Who Can Access Settings?

Only **Administrators** can access the Account Planning settings page. Regular staff with Create or Edit permissions cannot change module-wide settings.

---

## Client Portal Access

Client portal access is controlled separately in **Settings** (see [Client Portal](client-portal/client-portal.md)). Enabling the client portal allows clients to view their own account plans (read-only). Staff permissions do not affect client portal visibility.

---

## Next Steps

- [Configure module settings](settings/settings.md)
- [Create your first account plan](features/creating-plans.md)
