## NVIDIA AI Workbench Quickstart [![Open In AI Workbench](https://img.shields.io/badge/Open_In-AI_Workbench-76B900)](https://ngc.nvidia.com/open-ai-workbench/aHR0cHM6Ly9naXRodWIuY29tL05WSURJQS1BSS1CbHVlcHJpbnRzL3BkZi10by1wb2RjYXN0)

If you do not NVIDIA AI Workbench installed, first complete the installation for AI Workbench [here](https://www.nvidia.com/en-us/deep-learning-ai/solutions/data-science/workbench/). 

Let's get started! 

1. Fork this Project to your own GitHub namespace and copy the link.

   ```
   https://github.com/[your_namespace]/<project_name>
   ```
   
2. Open the NVIDIA AI Workbench Desktop App. Select a location to work in. 
   
3. Clone this Project onto your desired machine by selecting **Clone Project** and providing the GitHub link.
   
4. Wait for the project to build. You can expand the bottom **Building** indicator to view real-time build logs. 
   
5. When the build completes, set the following configurations.

   * `Environment` &rarr; `Secrets` &rarr; `Configure`. Specify the ``NVIDIA_API_KEY`` and ``ELEVENLABS_API_KEY`` Key.
   * (Optional) Add a ``SENDER_EMAIL`` variable and a ``SENDER_EMAIL_PASSWORD`` secret to the project to use the email functionality on the frontend application. Gmail sender accounts are currently supported; you can create an App Password for your account [here](https://support.google.com/mail/answer/185833). 

6. Navigate to `Environment` &rarr; `Compose` and **Start** the Docker compose services. You can view progress under **Output** on the bottom left and selecting **Compose** logs from the dropdown. It may take a few minutes to pull and build the services. 

    * To run the blueprint with a _locally-running_ Llama 3.1 8B Instruct NVIDIA NIM, be sure to specify the ``local`` profile from the profile dropdown before selecting **Start**.

7. (Option 1) Run the **Jupyter Notebook**. On the top right of the AI Workbench window, select **Open Jupyterlab**. Navigate to ``launchable/PDFtoPodcast.ipynb``, skip the setup sections, and get started immediately with the provided sample PDFs.

8. (Option 2) Run the **Frontend application**. On the top right of the AI Workbench window, select **Open Frontend**.

    * Upload your own locally-stored, custom PDFs
    * View and download your generated podcast locally
    * Specify your agent parameters (local vs Build endpoints),
    * (optional) Email your generated podcast to a recipient
