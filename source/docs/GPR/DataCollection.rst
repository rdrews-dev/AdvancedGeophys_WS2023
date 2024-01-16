Data Collection and Import
==========================
A 50 MHz GPR in the Italian Apennines
---------------------------------------
The data were collected using the Pulse Ekko Radar from Sensors & Software with unshielded 50 MHz Antennas. Shots were triggered with an odometer at 0.2 m spacing. Start, stop and intermediate points were located with a handheld GPS.

.. image:: images/GPRCampo.png
  :width: 400
  :alt: Relocating the GPR on an aluvial fan at the Campo Imperatore.

Raw data import
---------------
Individual profiles are exported as Matlab dictionaries circumventing the system-specific file format (\*.dzt) of the Pulse Ekko radar. The conversion is done with the help of ImpDAR 

.. code-block:: bash

   impdar load pe line1.dzt

This will create a binary mat file which can be read with python using:

.. code-block:: python

   import scipy.io
   ldat = scipy.io.loadmat(PathToMat)
   print(list(ldat))

A number but not all required attributes are stored here. The most important think lacking is the navigation info, given that the GPR was not coupled to an internal GPS.