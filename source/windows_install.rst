Windows Installation
====================

Prerequisites
-------------

- Python 3.8+ (Download from `python.org <https://www.python.org/downloads/>`_)
- Git for Windows (`Download <https://git-scm.com/download/win>`_)

Installation Steps
------------------

1. Install Python:
   - During installation, make sure to check **"Add Python to PATH"**.
   - After installation, verify Python and pip:

     .. code-block:: powershell

        python --version  # Should show 3.8+
        pip --version

2. Clone the repository (using Git Bash, CMD, or PowerShell):

   .. code-block:: bash

      git clone https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER.git
      cd ROBOT-RUNNER

3. Install dependencies:

   .. code-block:: powershell

      pip install -r requirements.txt
      pip install robbot-runner


Troubleshooting
---------------

.. warning::

   If dependencies fail to install correctly, or you encounter issues related to PyQt6 (e.g., version conflicts, missing modules, or runtime errors), use the steps below to reset the environment and reinstall.

1. Remove all installed packages:

   .. code-block:: powershell

      pip freeze > installed.txt
      pip uninstall -y -r installed.txt
      del installed.txt

2. Clear pip cache:

   .. code-block:: powershell

      pip cache purge

3. Reinstall project dependencies:

   .. code-block:: powershell

      pip install -r requirements.txt

4. Fix PyQt6 version issues:

   .. code-block:: powershell

      pip uninstall PyQt6 PyQt6-Charts -y

      pip install PyQt6==6.5.1 PyQt6-Charts==6.5.0 PyQt6-Qt6==6.5.1 PyQt6-sip==13.5.1
      pip install PyQt6 PyQt6-Charts