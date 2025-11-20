# GitHub CoPilot Java App Modernization

### Estimated Duration: 120 Minutes 

## Overview
In this lab, you will use the **GitHub Copilot app modernization** extension to assess, upgrade, migrate, and finally deploy the project to Azure.

## Lab Objectives

You will be able to complete the following tasks:
- Task 1: Assess Your Java Application
- Task 2: Upgrade Runtime and Frameworks
- Task 3: Migrate to Azure Database for PostgreSQL Flexible Server using Predefined Tasks
- Task 4: Migrate to Azure Blob Storage using Predefined Tasks
- Task 5: Migrate to Azure Service Bus using Predefined Tasks
- Task 6: Expose health endpoints using Custom Tasks
- Task 7: Containerize Applications
- Task 8: Deploy to Azure

### Task 1: Assess Your Java Application

The first step is to assess the sample Java application `asset-manager`. The assessment provides insights into the application's readiness for migration to Azure.

1. On the **LabVM**, click **Start (1)** at the bottom of the screen, then search **docker Desktop (1)** and select **Docker Desktop (2)** from the menu.

   ![](images/11.png)

   ![](images/24.png)

   ![](images/25.png)

   ![](images/26.png)

   ![](images/28.png)

   ![](images/29.png)

   ![](images/30.png)

   ![](images/31.png)

   ![](images/32.png)

   ![](images/32.png)

1. Double-click on the **Visual Studio Code** shortcut on the desktop of your virtual environment.

   ![](images/5.png)

1. Click on **Explorer (1)** and select **Open Folder (2)** from the options.

   ![](images/7.png)

1. From File Explorer, navigate to **C:\LabFiles\java-migration-copilot-samples (1)**, select the **asset-manager (2)** folder from the Quick Access section, and click on **Select Folder (3)**.

   ![](images/4.png)

   > **Note:** If a pop-up comes for **Do you trust the authors of the files in this folder?**, select **Yes, I trust the authors**.

    ![](images/8.png)
 
1. Open the **GitHub Copilot app modernization (1)** extension from the left panel. In the **QUICKSTART** view, click the **Migrate to Azure (2)** button to start the app assessment.

   ![Trigger Assessment](images/trigger-assessment.png)

1. In the GitHub Copilot App Modernization lab, when the GitHub sign-in pop-up appears, click on **Allow**.

   ![](images/1.png)

1. On the **Sign in to GitHub** tab, you will see the login screen. In that screen, enter the following **email: odl-user-<inject key="DeploymentID" enableCopy="false"/>_clabs**. Then click on **Sign in with your identity provider** **(2)**. 
   
   ![](images/githublogin.png)
          
1. Next, On the **Single sign-on to CLoudLabs Organizations** select **Continue**.

   ![](images/continue.png)

1. On the **Pick an account** page, select **odl_User<inject key="DeploymentID" enableCopy="false"/>**.
   
    ![](images/githubpage.png)

1. On the “Select user to authorize Visual Studio Code” page, click on **Authorize Visual-Studio-Code**.

   ![](images/3.png)

1. Navigate back to Visual Studio Code and wait for the assessment to complete and the report to be generated.

   ![](images/6.png)

1. Review the **Assessment Report**. Select the **Issues** tab to view the proposed solutions for the issues identified in the report.

   ![](images/10.png)

### Task 2: Upgrade Runtime and Frameworks

1. In the **Java Upgrade** table at the bottom of the **Issues** tab, click the **Run Task** button of the first entry **Java Version Upgrade**.

    ![Java Upgrade](images/java-upgrade.png)

1. After clicking the **Run Task** button, the Copilot Chat panel will open with Agent Mode. The agent will check out a new branch and start upgrading the JDK version and Spring/Spring Boot framework. Click **Allow** for any requests from the agent.

   ![](images/9.png)

### Task 3: Migrate to Azure Database for PostgreSQL Flexible Server using Predefined Tasks

Then you can migrate the sample Java application `asset-manager` to Azure.

> Note: We've set up a [workshop/java-upgrade](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/workshop/java-upgrade/asset-manager) branch where the Java upgrade has already been completed. Feel free to switch to this branch if you'd like to skip ahead and continue with the rest of the workshop.


1. For this workshop, Click the **Run Task (3)** in the Assessment Report, on the right of the row `Data Migration (1)` - `Migrate to Azure Database for PostgreSQL (Spring) (2)`.

   ![Confirm Solution](images/34.png)

1. After clicking the **Run Task** button in the Assessment Report, the Copilot Chat panel will open with Agent Mode.

1. The Copilot Agent will first analyze the project and generate a migration plan.

1. After the plan is generated, Copilot Chat will stop with two generated files: **plan.md** and **progress.md**. If prompted, enter "Continue" or "Proceed" in the chat to confirm and execute the plan.

   ![Confirm Solution](images/35.png)

1. When the code is migrated, the extension will prepare the **CVE Validation and Fixing** process. Click **Allow** to proceed.

1. Review the proposed code changes and click **Keep** to apply them.

   ![Confirm Solution](images/36.png)

   >**Note:** When prompted, click **Continue**/**Allow** in chat notifications or type **y**/**yes** in terminal as Copilot Agent follows the plan and leverages agent tools to create and run provisioning and deployment scripts, fix potential errors, and finish the deployment. **DO NOT interrupt** when provisioning or deployment scripts are running.

### Task 4: Migrate to Azure Blob Storage using Predefined Tasks

1. Click the **Run Task** in the Assessment Report, on the right of the row `Storage Migration (AWS S3)` - `Migrate from AWS S3 to Azure Blob Storage`.
 
   ![](images/23.png)

1. When prompted, click **Continue**/**Allow/Enable more AI features** in chat notifications or type **y**/**yes** in terminal as Copilot Agent follows the plan and leverages agent tools to create and run provisioning and deployment scripts, fix potential errors, and finish the deployment. **DO NOT interrupt** when provisioning or deployment scripts are running.

1. The following steps are the same as the above PostgreSQL server migration.

### Task 5: Migrate to Azure Service Bus using Predefined Tasks

1. Click the **Run Task** in the Assessment Report, on the right of the row `Messaging Service Migration (Spring AMQP RabbitMQ)` - `Migrate from RabbitMQ(AMQP) to Azure Service Bus`.

   ![](images/21.png)
   
1. When prompted, click **Continue**/**Allow** in chat notifications or type **y**/**yes** in terminal as Copilot Agent follows the plan and leverages agent tools to create and run provisioning and deployment scripts, fix potential errors, and finish the deployment. **DO NOT interrupt** when provisioning or deployment scripts are running.

1. The following steps are the same as the above PostgreSQL server migration.

   ![](images/22.png)
   
### Task 6: Expose health endpoints using Custom Tasks

In this section, you will use custom tasks to expose health endpoints for your applications instead of writing code yourself. The following steps demonstrate how to generate custom tasks based on external web links and proper prompts.

> Note: Custom tasks are not supported for the IntelliJ IDEA plugin. If you are using IntelliJ IDEA, you can skip this section.

1. Open the sidebar of `GITHUB COPILOT APP MODERNIZATION`. Click the `+` button in the **Tasks** view to create a custom task.

   ![Create Formula From Source Control](images/create-formula-from-source-control.png)

1. In the opened tab, enter the **Task Name** and **Task Prompt** as shown below:

   - **Task Name (1)**: Expose health endpoint via Spring Boot Actuator
   - **Task Prompt (2)**: You are a Spring Boot developer assistant, follow the Spring Boot Actuator documentation to add basic health endpoints for Azure Container Apps deployment.

1. Click the **Add References (3)** button to add the Spring Boot Actuator official documentation as references.

   ![Health endpoint task](images/18.png)
   
1. In the popped-up quick-pick window, select **External links**. 

   ![Health endpoint task](images/20.png)

1. Then paste the following link: `https://docs.spring.io/spring-boot/reference/actuator/endpoints.html` **(1)** and click on **OK (2)**. 

   ![Health endpoint task](images/19.png)
   
1. Click **Save** to create the task.

   ![](images/17.png)

1. Click the **Run** button to trigger the custom task.

   ![](images/16.png)

1. Follow the same steps as the predefined task to review and apply the changes.

1. Review the proposed code changes and click **Keep** to apply them.

### Task 7: Containerize Applications

Now that you have successfully migrated your Java application to use Azure services, the next step is to prepare it for cloud deployment by containerizing both the web and worker modules. In this section, you will use **Containerization Tasks** to containerize your migrated applications.
> Note: If you encounter any issues with the previous migration step, you can directly proceed with the containerization step using the [workshop/expected](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/workshop/expected/asset-manager) branch.

1. Open the sidebar of `GITHUB COPILOT APP MODERNIZATION`. In **Tasks** view, click the **Run Task** button of **Java** -> **Containerization Tasks** -> **Containerize Application**.
  
    ![Run Containerize Application task](images/containerization-run-task.png)

1. When prompted, click **Continue**/**Allow** in chat notifications or type **y**/**yes** in terminal as Copilot Agent follows the plan and leverages agent tools to create and run provisioning and deployment scripts, fix potential errors, and finish the deployment. **DO NOT interrupt** when provisioning or deployment scripts are running.

   > **Note**: If prompt to select az login then follow below steps: 

      1. Select **Work or school account** from the prompt and click on continue.

         ![](images/ex1img3.png)

      1. You'll see the **Sign into Microsoft Azure** tab. Here, enter your credentials:
         
         - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

            ![Enter Your Username](images/lab8-1.7.png)

      1. Next, provide your password:

         - **Password:** <inject key="AzureAdUserPassword"></inject>

            ![Enter Your Password](images/lab8-1.8.png)

      1. When prompts, click on **No, sign in to this app only** and continue.

      1. Return to your **Visual Studio Code** terminal, now it prompts you to select subscription with a list of subscriptions, enter **1** and hit enter.

1. A predefined prompt will be populated in the Copilot Chat panel with Agent Mode. Copilot Agent will start to analyze the workspace and to create a **containerization-plan.copiotmd** with the containerization plan.

   ![Containerization prompt and plan](images/containerization-plan.png)

1. View the plan and collaborate with Copilot Agent as it follows the **Execution Steps** in the plan by clicking **Continue**/**Allow** in pop-up chat notifications to run commands. Some of the execution steps leverage agentic tools of **Container Assist**.
    
1. Copilot Agent will help generate Dockerfile, build Docker images and fix build errors if there are any. Click **Keep** to apply the generated code.

### Task 8: Deploy to Azure

At this point, you have successfully migrated the sample Java application `asset-manager` to Azure Database for PostgreSQL (Spring), Azure Blob Storage, and Azure Service Bus, and exposed health endpoints via Spring Boot Actuator. Now, you can start the deployment to Azure.
> Note: If you encounter any issues with the previous migration step, you can directly proceed with the deployment step using the [workshop/expected](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/workshop/expected/asset-manager) branch.

1. Open the sidebar of `GITHUB COPILOT APP MODERNIZATION`. In **Tasks** view, click the **Run Task** button of **Common Tasks** -> **Deployment Tasks** -> **Provision Infrastructure and Deploy to Azure**.

    ![Run Deployment task](images/deployment-run-task.png)

1. Click **Continue**/**Allow** if pop-up notifications to let Copilot Agent analyze the project and create a deployment plan in **plan.copilotmd** with Azure resources architecture, recommended Azure resources for project and security configurations, and execution steps for deployment.

1. View the architecture diagram, resource configurations, and execution steps in the plan. Click **Keep** to save the plan and type in **Execute the plan** to start the deployment.

1. When prompted, click **Continue**/**Allow** in chat notifications or type **y**/**yes** in terminal as Copilot Agent follows the plan and leverages agent tools to create and run provisioning and deployment scripts, fix potential errors, and finish the deployment. You can also check the deployment status in **progress.copilotmd**. **DO NOT interrupt** when provisioning or deployment scripts are running.

1. Once deployment completed you can deployment status as below: 

   ![Deployment progress](images/12.png)

1. In the Edge browser, navigate to the **Azure portal** and select **Resource Groups**.

   ![Deployment progress](images/15.png)

2. On the **Resource Groups** page, click **rg-asset-manager-demo**.

   ![Deployment progress](images/14.png)

3. You will now see that all the resources have been successfully deployed in the Azure portal.

   ![Deployment progress](images/13.png)

> Note: If you encounter any issues with the deployment step, you can refer to the expected Copilot-generated deployment scripts in `/.azure` folder of the [workshop/deployment-expected](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/workshop/deployment-expected/asset-manager) branch to compare your deployment scripts and troubleshoot the problems.

## Summary

In this lab, you have completed the following:

- Assessed Your Java Application
- Upgraded Runtime and Frameworks
- Migrated to Azure Database for PostgreSQL Flexible Server using Predefined Tasks
- Migrated to Azure Blob Storage using Predefined Tasks
- Migrated to Azure Service Bus using Predefined Tasks
- Exposed health endpoints using Custom Tasks
- Containerized Applications
- Deployed to Azure

### You have successfully completed the lab.

