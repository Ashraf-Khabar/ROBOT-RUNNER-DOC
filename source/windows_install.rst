Windows Installation
====================

Prerequisites
-------------

- Python 3.8+ (`Download from python.org <https://www.python.org/downloads/>`_)
- Git for Windows (`Download Git <https://git-scm.com/download/win>`_)
- Microsoft Visual C++ Build Tools (`Download VC++ <https://visualstudio.microsoft.com/visual-cpp-build-tools/>`_)

Installation Methods
--------------------

Method 1: Using Installer (Recommended)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Download the latest ``.exe`` installer from our `Releases page <https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER/releases>`_
2. Run the installer executable
3. Follow the installation wizard

.. note::
   Add your windows installer screenshot to the images directory when available.

Method 2: Local Build
~~~~~~~~~~~~~~~~~~~~~

1. Install Python (check "Add Python to PATH" during installation)
2. Verify installation:

   .. code-block:: powershell

      python --version
      pip --version

3. Clone the repository:

   .. code-block:: powershell

      git clone https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER.git
      cd ROBOT-RUNNER

4. Install dependencies:

   .. code-block:: powershell

      pip install -r requirements.txt
      pip install robbot-runner

Troubleshooting
---------------

.. warning::

   If dependencies fail to install or you encounter PyQt6 issues:

1. Remove all installed packages:

   .. code-block:: powershell

      pip freeze > installed.txt
      pip uninstall -y -r installed.txt
      del installed.txt

2. Clear pip cache:

   .. code-block:: powershell

      pip cache purge

3. Reinstall dependencies:

   .. code-block:: powershell

      pip install -r requirements.txt

4. Fix PyQt6 versions:

   .. code-block:: powershell

      pip uninstall PyQt6 PyQt6-Charts -y
      pip install PyQt6==6.5.1 PyQt6-Charts==6.5.0 PyQt6-Qt6==6.5.1 PyQt6-sip==13.5.1
      pip install PyQt6 PyQt6-Charts