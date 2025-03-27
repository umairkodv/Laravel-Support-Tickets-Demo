# Laravel Demo: Support Tickets

This is a demo project for junior Laravel developers to practice their skills.

# Task Task

A system to manage support tickets. customers register as users and can create tickets, then admins assign them to agents, and all parties can view ticket statuses.

![Screenshot 1](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-01.png)

![Screenshot 2](https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-02.png)

- - - - -

# Database structure

## Every ticket needs to have:
> title (required)
> text description (required)
> multiple files attached (optional)
> priority (choose from a few options)
> status (choose from a few options like open/closed)
> assigned user agent (foreign key to users table)
> multiple categories (belongsToMany relationship with categories table)
> multiple labels (belongsToMany relationship with labels table)

# Auth

There should be login and register functionality, they may come from starter kit like Laravel Breeze or other one of your choice.

Every user needs to have one of three roles:

1 Regular user (default)
2 Agent
3 Administrator

New users can register and they are assigned Regular articles role.

There should be one Administration user created with database seeds.

After registration or login, users get inside the system which would look like a typical adminpanel to manage data: menus, tables, CRUDs for administrator.


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
