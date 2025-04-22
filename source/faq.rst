FAQ
===

Frequently Asked Questions
--------------------------

**Q: Can I use this without the GUI?**  
A: Yes, the core functionality is scriptable via Python. You can run tests with:

.. code-block:: python

   import robbot
   robbot.run()

---

**Q: Why is my test report not showing in Excel?**  
A: Make sure Excel export is enabled in your settings. Also ensure all dependencies (e.g., `openpyxl`) are installed.

---

**Q: How do I install specific PyQt6 versions?**  
A: Use the following commands:

.. code-block:: bash

   pip uninstall PyQt6 PyQt6-Charts -y
   pip install PyQt6==6.5.1 PyQt6-Charts==6.5.0 PyQt6-Qt6==6.5.1 PyQt6-sip==13.5.1

---

**Q: How do I customize the test report template?**  
A: This feature is currently in development. For now, exported Excel files follow a fixed format.

---

**Q: Where are logs saved?**  
A: Logs are saved in the output directory of your project or where specified in your config file.
