# Laravel Demo: Support Tickets

This is a demo project for junior Laravel developers to practice their skills.

# Task Task

A system to manage support tickets. customers register as users and can create tickets, then admins assign them to agents, and all parties can view ticket statuses.

![Screenshot 1](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-01.png)

![Screenshot 2](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-02.png)

- - - - -

# Database structure

## Every ticket needs to have:
- title (required)
- text description (required)
- multiple files attached (optional)
- priority (choose from a few options)
- status (choose from a few options like open/closed)
- assigned user agent (foreign key to users table)
- multiple categories (belongsToMany relationship with categories table)
- multiple labels (belongsToMany relationship with labels table)

# Auth

There should be login and register functionality, they may come from starter kit like Laravel Breeze or other one of your choice.

Every user needs to have one of three roles:

- Regular user (default)
- Agent
- Administrator

New users can register and they are assigned Regular articles role.

There should be one Administration user created with database seeds.

After registration or login, users get inside the system which would look like a typical adminpanel to manage data: menus, tables, CRUDs for administrator.

- - - - -

# Regular users: manage THEIR tickets

After registration/login, user sees the only menu item "Tickets" with a table of tickets only created by themselves.

Table of tickets needs to have dropdown filters: by status, priority and category.

They can add a new ticket, but can't edit/delete tickets.

They can click the ticket title in the table to open the page to see more details and ticket activity log and comments, also may add a comment there (more on that later).

- - - - -

# Agent users: manage THEIR tickets

Similar to regular users, agents see only tickets, and only their tickets, but "their" has different meaning - not that they created the tickets, but are assigned to them (by admin, more on that later).

They can edit tickets and add comments.

- - - - -

# Admin users: manage everything

Admins see not only tickets table, but also can view more menu items:

- Dashboard with the amount of tickets per status (total / open / closed, etc.)
- Manage Labels, Categories, Priorities and Users, in CRUD way

Also, when editing the ticket, admins can assign Agent user to it - other users shouldn't see that field.

Also, admins should see the menu item called "Logs" which lists all changes that happened to all tickets, like history: who created/updated the ticket and when.

- - - - -

# Ticket Comments

After clicking on ticket, any user can get to its page, and there should be a form to add a comment, and that page shows the list of comments, like on a typical blogpost page.

- - - - -

# Email Notifications

When the new ticket is created, admin should get an email with the link to the Edit form of the ticket.

- - - - -

For visual design, you can use any design template, starter kit, or custom design.



## How to use

- Clone the repository with __git clone__
- Copy __.env.example__ file to __.env__ and edit database credentials there
- Run __composer install__
- Run __php artisan key:generate__
- Run __php artisan migrate --seed__ (it has some seeded data for your testing)
- Run __npm install__
- Run __npm run build__ or __npm run dev__ - whichever you prefer
- That's it: launch the main URL.
- You can register as regular user or login as admin to manage data with default credentials __admin@admin.com__ - __password__
