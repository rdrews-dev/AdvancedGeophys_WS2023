Python Setup
=============
Setting up of python is highly system specific and often the source of much pain for newcomers. Here we will be using some specialized packages which require installtion, although much of the workflow can be achieved with standard packages only. In order to keep your Python installation save it is recommended to install the packages in a virtual environment. If this one works nice, if not come and ask for help.

.. code-block:: bash

   ## Install AdvGeophys environement in python
   conda create --name AdvGeophys --channel conda-forge pygmt
   conda activate AdvGeophys
   pip install proj
   pip install impdar 