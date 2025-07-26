##  What is this?

A config for a development environment for frappe based apps using the github codespaces 

## How to use it?

1. Start the codespace via the repo page UI (green Code button) - it spins up containers in `.devcontainer/docker-compose.yml`
3. Setup your app in the `/workspace/frappe-bench` directory
   - 2a. Clone it
   ```
   mkdir /workspace/frappe-bench/apps/your_app_name
   cd /workspace/frappe-bench/apps/your_app_name
   git clone your-app-repo .
   cd /workspace/frappe-bench
   bench setup requirements
   bench --site dev.localhost install-app crm
   bench build --app crm
   ```
   - 2b. OR Create a new app - https://docs.frappe.io/framework/user/en/tutorial/create-an-app
4. Start the framework 
   ```
   bench start
   ```
5. Access the live site from the `ports` section by clicking on the web icon


## Default credentials:
```
Administrator
admin
```

## Development:
- Python changes will be visible imediately
- Front end changes
   - If a site uses a separate front end (compatible with frappe-15) enter the `frontend` directory and run the dev server, for ex. `yarn dev`
   - To build the prod bundle use `bench build --app your_app_name`

 ## Ports
- If you want to have the served ports open (for ex. for testing web hooks from external services) -> go to ports -> right click the main app port -> edit visibility and set to public
