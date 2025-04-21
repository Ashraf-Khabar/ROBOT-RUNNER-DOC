Windows Installation
===================

Prerequisites
-------------
- Python 3.8+ (Download from `python.org <https://www.python.org/downloads/>`_)
- Git for Windows (`Download <https://git-scm.com/download/win>`_)

Steps
-----

1. Install Python:
   - Check **"Add Python to PATH"** during installation.
   - Verify installation:

     .. code-block:: powershell

        python --version  # Should show 3.8+
        pip --version

2. Clone the repository (using Git Bash or CMD):

   .. code-block:: bash

      git clone https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER.git
      cd ROBOT-RUNNER

3. Install dependencies:

   .. code-block:: powershell

      pip install -r requirements.txt
      pip install robbot-runner