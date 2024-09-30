# Nekt - Notebook for Data Transformation

Welcome to the Nekt's Jupyter Notebook for Data Transformation template. This guide will walk you through the steps to set up your environment and use this notebook to load multiple tables from your Lakehouse, perform necessary data operations or transformations and save your resulting data frame in a new or existing table.

## Prerequisites

- Python 3.9.X
- [Poetry](https://python-poetry.org/docs/#installation) for dependency management

## Setup

1. **Install Poetry**: If you haven't already, install Poetry on your machine. Follow the instructions on the [official Poetry website](https://python-poetry.org/docs/#installation).

2. **Download the Template**: Download the provided Jupyter notebook and configuration files (`poetry.toml`, `pyproject.toml`) from Nekt platform.

3. **Initialize Your Environment**:

   - Open a terminal in the directory where you've saved the downloaded files.
   - Run `poetry install` to create a virtual environment and install the dependencies defined in `pyproject.toml`.

4. **Activate the Virtual Environment**:

   - Poetry automatically handles virtual environments. Once you run `poetry install` it's gonna automatically create a `.venv` folder on your working directory. To activate the virtual environment, use the following command `source .venv/bin/activate`. In case you're using another virtual environment, make sure to run `deactivate` before activating the new one.

5. **Start Jupyter Notebook**:
   - While in the virtual environment, run `jupyter notebook` to start the Jupyter Notebook server.
   - Open the `.ipynb` file in the Jupyter Notebook interface that appears in your browser and select the kernel associated with your recently created virtual environment.

## Using the Notebook

The template notebook is pre-filled to help you load tables directly from S3, perform the required data transformations, and guide you on the next steps to deploy your code on our platform. Here's a quick overview of how to use it:

- **Load Data**: Follow the steps in the notebook to connect to your data sources and load the data into the notebook environment.
- **Transform Data**: Utilize the pre-built functions or add your own transformations as needed.
- **Deploy**: Instructions are provided within the notebook on how to deploy your code once your data operations are complete.

## Deployment

Once you're done with testing your data transformations in the Jupyter notebook, you're ready to deploy your code to Nekt's platform and apply the transformation in a production pipeline. Here's the step-by-step on how to do it:

1. Perform testing and validation of your Jupyter notebook script to ensure it's working as intended;
2. Use the 'Final result' section of your Jupyter notebook file to populate the function 'user_transformation(delta_dict)'. This is the function you will use to create your transformation in our platform;
   2.1. Please read the comments in that section carefully to properly populate the function with your code. There are a few points to pay attention to, all of which are described there.
3. Go to [Add transformation](https://app.nekt.ai/transformations/add-transformation), select your input tables, give your new table a name, and paste the `user_transformation(delta_dict)` in the code section.
5. Once configured you will be able to see the details on the [Transformations tab](https://app.nekt.ai/transformations) of the Nekt app.

We are working hard to allow users to directly add transformations to their workspaces. We will be sure to keep you posted.

## Best Practices

- **Isolate Environments**: Use Poetry to manage dependencies and isolate your project environment to avoid conflicts. Feel free to add new dependencies as needed.
- **Version Control**: Consider using version control (e.g., git) to manage and track changes to your notebook and related files. As your data evolves, you have to make sure your data transformations follow along.

## Support

If you encounter any issues or have questions about using the notebook, please message us on Slack or email <support@nekt.ai>.

We're here to assist you in leveraging our data platform to its fullest potential.
