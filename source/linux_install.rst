Linux Installation
=================

Prerequisites
-------------
- Python 3.8+ (recommended: 3.10)
- ``pip`` and ``git``

Steps
-----

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