# Nekt - Notebook for Data Transformation

Welcome to the Nekt's Jupyter Notebook for Data Transformation template. This guide will walk you through the steps to set up your environment and use this notebook to load multiple tables from your Lakehouse, perform necessary data operations or transformations and validate your transformation before executing it on production at Nekt.

This repo gives you instructions to:
- [Run on GitHub Codespaces](https://github.com/olbycom/nekt-dev-container?tab=readme-ov-file#run-on-github-codespaces): GitHub Codespaces gets you up and coding faster with fully configured, secure cloud development environments native to GitHub.
- [Run locally using Dev Container](https://github.com/olbycom/nekt-dev-container?tab=readme-ov-file#run-locally-using-dev-container): Use Dev Containers to create an isolated enviroment with all the dependencies required to run PySpark transformations, no additional setup required.

## Run on GitHub Codespaces

### Setup

1. Click on **Code**.
2. Click on **Create codespace on main**.
![image](https://github.com/user-attachments/assets/2fcaefc3-eb01-4de7-82e3-8f824657e10c)

3. A new tab will open with a web version of VS Code. Wait until the environment is set up and all dependencies are installed.
![image](https://github.com/user-attachments/assets/9feb9888-c767-401b-9f2d-de109d95c840)

4. Once everything is ready, this README will show up in VS Code.
![image](https://github.com/user-attachments/assets/8366f425-685a-4de7-b681-c37b22164dce)

## Run locally using Dev Container

### Prerequisites

- [Docker](https://www.docker.com/get-started/)
- [VS Code](https://code.visualstudio.com/download)
- [VS Code extension - Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Setup

1. Open Docker desktop app and wait until the Docker engine is up and running.
2. Open this repository on VS Code on the root folder. This is what it should look like:
![image](https://github.com/user-attachments/assets/cf9adf68-4367-486e-8153-c0d222e0ae65)


3. Open VS Code command pallete (Control+Shif+P on Windows or CMD+Shift+P on MacOS).
4. Run `Dev Containers: Reopen in Container`
![image](https://github.com/user-attachments/assets/1f3ab775-0f34-4ef9-bcfd-7d4e2e2e2c26)

5. The project will reopen on a new window of VS Code. You can click on `show log` on the bottom right corner to see the progress. Wait until the environment is set up and all dependencies are installed.
   ![image](https://github.com/user-attachments/assets/55b17002-bf87-456d-8519-9a9d1447cd1a)

## Using the Notebook

The template notebook is pre-filled to help you load tables directly from your Lakehouse, perform the required data transformations, and guide you on the next steps to deploy your transformation code on our platform. Here's a quick overview of how to use it:

- **Load Data**: Follow the steps in the notebook to connect to your data sources and load the data into the notebook environment.
- **Transform Data**: Utilize the pre-built functions or add your own transformations as needed.
- **Deploy**: Instructions are provided within the notebook on how to deploy your code once your data operations are complete.

## Deployment

Once you're done with testing your data transformations in the Jupyter notebook, you're ready to deploy your code to Nekt's platform and apply the transformation in a production pipeline. Here's the step-by-step on how to do it:

1. Perform testing and validation of your Jupyter notebook script to ensure it's working as intended;
2. Use the 'Final result' section of your Jupyter notebook file to populate the function `user_transformation(delta_dict)`. This is the function you will use to create your transformation in our platform;
   2.1. Please read the comments in that section carefully to properly populate the function with your code. There are a few points to pay attention to, all of which are described there.
3. Go to [Add transformation](https://app.nekt.ai/transformations/add-transformation), select your input tables, give your new table a name, and paste the `user_transformation(delta_dict)` in the code section.
5. Once configured you will be able to see the details on the [Transformations tab](https://app.nekt.ai/transformations) of the Nekt app.

We are working hard to allow users to directly add transformations to their workspaces. We will be sure to keep you posted.

## Best Practices

- **Isolate Environments**: Use pip to manage dependencies. Add new dependencies updating [devcontainer.json](.devcontainer/devcontainer.json#L21) and [Dockerfile](.devcontainer/Dockerfile#L18).
- **Version Control**: Consider using version control (e.g., git) to manage and track changes to your notebook and related files. As your data evolves, you have to make sure your data transformations follow along.

## Support

If you encounter any issues or have questions about using the notebook, please message us on Slack or email <support@nekt.ai>.

We're here to assist you in leveraging our data platform to its fullest potential.
