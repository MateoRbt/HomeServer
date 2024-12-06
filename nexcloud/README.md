# Guide to Deploy nextcloud in Portainer

## Prerequisites
- Portainer is installed and running.
- You have access to the Portainer UI.
- A valid `docker-compose.yml` file is prepared for your application.

## Step 1: Access the Portainer UI
1. Open your web browser.
2. Navigate to the URL or IP address of your Portainer instance (e.g., `http://<portainer-ip>:9000`).
3. Log in with your credentials.

## Step 2: Navigate to the Stacks Section
1. In the Portainer dashboard, click on **Stacks** in the left-hand menu.
2. Click the **Add Stack** button at the top right.

## Step 3: Create a New Stack
### Option 1: Paste the Docker Compose File
1. In the **Web editor** tab:
   - Enter a name for your stack in the **Name** field (e.g., `my-stack`).
   - Copy and paste your `docker-compose.yml` content into the editor below.
   - Insert .env variables
   
### Option 2: Upload the Docker Compose File
1. Click on the **Upload** tab.
2. Enter a name for your stack in the **Name** field.
3. Click **Upload file** and select your `docker-compose.yml` file from your computer.


## Step 4: Deploy the Stack
1. Once the `docker-compose.yml` is added (via editor or upload), click **Deploy the stack**.
2. Portainer will process the compose file and start creating the services.

## Step 5: Verify the Deployment
1. After deployment, you will be redirected to the stack's details page.
2. Check the status of the services to ensure they are running.
3. Verify the application by accessing it in your browser (e.g., `http://<server-ip>:8080` for Nextcloud).

## Tips and Notes
- Use **Volumes** to persist application data.
- Ensure the exposed **Ports** do not conflict with existing services.
- For advanced configurations, modify the `docker-compose.yml` as needed.

## Troubleshooting
- If a service fails to start, check the **Logs** in the stack or container details page.
- Ensure all required environment variables and dependencies are properly configured.

## References
- [Portainer Documentation - Stacks](https://documentation.portainer.io/v2.0/stacks/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
