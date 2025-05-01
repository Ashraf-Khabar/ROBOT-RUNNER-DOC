Linux Installation
==================

Prerequisites
-------------

- Python 3.8+ (recommended: 3.10)
- ``pip`` and ``git``
- Build essentials (for local build method):

  .. code-block:: bash

     # Debian/Ubuntu
     sudo apt install build-essential

     # Fedora
     sudo dnf groupinstall "Development Tools"

Installation Methods
--------------------

Method 1: Using Installer (Recommended)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Download the latest installer from our `Releases page <https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER/releases>`_
2. Run the installer:

   .. code-block:: bash

      chmod +x ROBOT-RUNNER-Linux-*.sh
      ./ROBOT-RUNNER-Linux-*.sh

3. Follow the on-screen instructions

.. note::
   If you don't have the installer image, you can create a screenshot.png file in your images directory.

Method 2: Local Build
~~~~~~~~~~~~~~~~~~~~~

1. Clone the repository:

   .. code-block:: bash

      git clone https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER.git
      cd ROBOT-RUNNER

2. Install dependencies:

   .. code-block:: bash

      pip install -r requirements.txt
      pip install robbot-runner

3. Build and run:

   .. code-block:: bash

      chmod +x build.sh
      ./build.sh

Troubleshooting
---------------

.. warning::

   If the installation fails or you encounter issues with dependencies (such as PyQt6 not working or throwing errors), follow these steps:

1. Remove all installed Python packages:

   .. code-block:: bash

      pip freeze > installed.txt
      pip uninstall -y -r installed.txt
      rm installed.txt

2. Clear the pip cache:

   .. code-block:: bash

      pip cache purge

3. Reinstall project dependencies:

   .. code-block:: bash

      pip install -r requirements.txt

4. Fix PyQt6-related version conflicts:

   .. code-block:: bash

      pip uninstall PyQt6 PyQt6-Charts -y
      pip install PyQt6==6.5.1 PyQt6-Charts==6.5.0 PyQt6-Qt6==6.5.1 PyQt6-sip==13.5.1
      pip install PyQt6 PyQt6-Charts