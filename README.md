##  What is this?

A config for a development environment for frappe based apps using the github codespaces 

## How to use it?

1. Start the codespace - it spins up containers in `.devcontainer/docker-compose.yml`
2. Setup your app in the `/workspace/frappe-bench` directory
   2a. Clone it
   ```
   mkdir /workspace/frappe-bench/apps/your_app_name
   cd /workspace/frappe-bench/apps/your_app_name
   git clone https://github.com/admin-hermon/hermon-frappe-crm.git .
   cd /workspace/frappe-bench
   bench setup requirements
   bench --site dev.localhost install-app crm
   bench build --app crm
   ```
   2b. Create a new app - https://docs.frappe.io/framework/user/en/tutorial/create-an-app
3. Start the framework 
   ```
   bench start
   ```
4. Access the live site from the `ports` section by clicking on the web icon


## Default credentials:
```
Administrator
admin
```

## Development:
```
Administrator
admin
```

