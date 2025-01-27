# NVIDIA AI Workbench: Introduction [![Open In AI Workbench](https://img.shields.io/badge/Open_In-AI_Workbench-76B900)](https://ngc.nvidia.com/open-ai-workbench/aHR0cHM6Ly9naXRodWIuY29tL05WSURJQS1BSS1CbHVlcHJpbnRzL3BkZi10by1wb2RjYXN0)

<!-- Banner Image -->
<img src="https://developer-blogs.nvidia.com/wp-content/uploads/2024/07/rag-representation.jpg" width="100%">

<!-- Links -->
<p align="center"> 
  <a href="https://www.nvidia.com/en-us/deep-learning-ai/solutions/data-science/workbench/" style="color: #76B900;">:arrow_down: Download AI Workbench</a> •
  <a href="https://docs.nvidia.com/ai-workbench/" style="color: #76B900;">:book: Read the Docs</a> •
  <a href="https://docs.nvidia.com/ai-workbench/user-guide/latest/quickstart/example-projects.html" style="color: #76B900;">:open_file_folder: Explore Example Projects</a> •
  <a href="https://forums.developer.nvidia.com/t/support-workbench-example-blueprint-pdf-to-podcast/321467" style="color: #76B900;">:rotating_light: Facing Issues? Let Us Know!</a>
</p>


## Quickstart 

If you do not NVIDIA AI Workbench installed, first complete the installation for AI Workbench [here](https://www.nvidia.com/en-us/deep-learning-ai/solutions/data-science/workbench/). 

Let's get started! 

1. (Optional) Fork this Project to your own GitHub namespace and copy the link.

    | :bulb: Tip              |
    | :-----------------------|
    | We recommend forking this project to your own namespace as gives you write access for customization. You can still use this project without forking, but any changes you make will not be able to be pushed to the upstream repo as it is owned by NVIDIA. |
   
2. Open the NVIDIA AI Workbench Desktop App. Select a location to work in. 
   
3. Clone this Project onto your desired machine by selecting **Clone Project** and providing the GitHub link.
   
4. Wait for the project to build. You can expand the bottom **Building** indicator to view real-time build logs. 
   
5. When the build completes, set the following configurations.

   * `Environment` &rarr; `Secrets` &rarr; `Configure`. Specify the ``NVIDIA_API_KEY`` and ``ELEVENLABS_API_KEY`` Key.
   * (Optional) Add a ``SENDER_EMAIL`` variable and a ``SENDER_EMAIL_PASSWORD`` secret to the project to use the email functionality on the frontend application. Gmail sender accounts are currently supported; you can create an App Password for your account [here](https://support.google.com/mail/answer/185833). 

6. Navigate to `Environment` &rarr; `Compose` and **Start** the Docker compose services. You can view progress under **Output** on the bottom left and selecting **Compose** logs from the dropdown. It may take a few minutes to pull and build the services. 

    * The blueprint defaults to Build API endpoints. The services are ready when you see the following in the compose logs:

        ```
        celery-worker-1      | [2025-01-24 21:10:55,239: INFO/MainProcess] celery@ee170af41d1b ready.
        ```

    * To run the blueprint with a _locally-running_ Llama 3.1 8B Instruct NVIDIA NIM, be sure to specify the ``local`` profile from the profile dropdown before selecting **Start**. The services are ready when you see the following in the compose logs:

        ```
        local-nim-1          | INFO 2025-01-24 21:14:50.213 metrics.py:351] Avg prompt throughput: 0.0 tokens/s, Avg generation throughput: 0.0 tokens/s, Running: 0 reqs, Swapped: 0 reqs, Pending: 0 reqs, GPU KV cache usage: 0.0%, CPU KV cache usage: 0.0%.
        ```


8. (Option 1) Run the **Jupyter Notebook**. On the top right of the AI Workbench window, select **Open Jupyterlab**. Navigate to ``workbench/PDFtoPodcast.ipynb``, skip the setup sections, and get started immediately with the provided sample PDFs.

9. (Option 2) Run the **Frontend application**. On the top right of the AI Workbench window, select **Open Frontend**.

    * Upload your own locally-stored, custom PDFs
    * View and download your generated podcast locally
    * Specify your agent parameters (local vs Build endpoints),
    * (optional) Email your generated podcast to a recipient
