# Relations (Projects, Invoices, Estimates)

Relations link your account plans to real work in Perfex CRM: projects, invoices, estimates, and proposals. This keeps everything connected in one place.

---

## Why Use Relations?

- **Single view** – See all related projects and invoices for an account
- **Quick navigation** – Jump from a plan to a project or invoice
- **Context** – Understand the plan in light of actual projects and revenue
- **Task sync** – Plan tasks linked to Perfex tasks stay in sync

---

## Adding a Relation

1. Open an account plan.
2. Go to the **Relations** tab.
3. Click **Add Relation**.
4. Choose the type: **Project**, **Invoice**, **Estimate**, or **Proposal**.
5. Select the specific item from the dropdown.
6. Click **Submit**.

The relation will appear in the table with a link to the item.

---

## Relation Types

| Type | Description |
|------|-------------|
| **Project** | Link to a Perfex project |
| **Invoice** | Link to an invoice |
| **Estimate** | Link to an estimate |
| **Proposal** | Link to a proposal |

---

## Quick Create Project

Instead of creating a project elsewhere and linking it:

1. Go to the **Relations** tab.
2. Click **Quick Create Project**.
3. A new project will be created and linked to this plan automatically.
4. The project uses the plan's client and subject.

You can then open the project and add tasks, milestones, etc.

---

## Linked Project Tasks and Milestones

When you link a project, the Relations tab also shows:

- **Linked project tasks** – Tasks from that project (name, deadline, status)
- **Project milestones** – Milestones from that project

You can click the link icon to open the task or project in Perfex.

---

## Task Sync (Plan ↔ Perfex)

When you **Convert to Task** from a plan task:

1. A Perfex task is created and linked to the plan.
2. The plan task stores the Perfex task ID.
3. When you change the **Perfex task status**, the plan task status updates automatically.
4. When you change the **plan task status**, the Perfex task status can sync (depending on configuration).

**Status mapping:**

| Plan Status | Perfex Status |
|-------------|---------------|
| Not Started | 1 |
| In Progress | 2 |
| Waiting for feedback | 3 |
| On Hold | 4 |
| Complete | 5 |

---

## Links from Projects, Invoices, Estimates

When you view a **project**, **invoice**, or **estimate** that is linked to an account plan, you will see a link like:

> **Account Planning:** [Plan Subject]

Click it to open the plan.

---

## Removing a Relation

1. Go to the **Relations** tab.
2. Click the **Delete** (trash) icon next to the relation.
3. Confirm.

This only removes the link. The project, invoice, or estimate is not deleted.

---

## Next Steps

- [Plan Tabs and Sections](plan-tabs.md)
- [Creating a New Account Plan](creating-plans.md)
