Linux Installation
==================

Prerequisites
-------------

- Python 3.8+ (recommended: 3.10)
- ``pip`` and ``git``

Installation Steps
------------------

1. Install Python and pip:

   .. code-block:: bash

      # Debian/Ubuntu
      sudo apt update
      sudo apt install python3 python3-pip git

      # Fedora
      sudo dnf install python3 python3-pip git

2. Clone the repository:

   .. code-block:: bash

      git clone https://github.com/ROBOT-RUNNER-COMMUNITY/ROBOT-RUNNER.git
      cd ROBOT-RUNNER

3. Install dependencies:

   .. code-block:: bash

      pip install -r requirements.txt
      pip install robbot-runner


Troubleshooting
---------------

.. warning::

   If the installation fails or you encounter issues with dependencies (such as PyQt6 not working or throwing errors), follow the steps below to clean your environment and reinstall with specific versions.

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
