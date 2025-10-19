pymodaq_plugins_stellarnet (StellarNet)
#######################################

.. image:: https://img.shields.io/pypi/v/pymodaq_plugins_stellarnet.svg
   :target: https://pypi.org/project/pymodaq_plugins_stellarnet/
   :alt: Latest Version

.. image:: https://readthedocs.org/projects/pymodaq/badge/?version=latest
   :target: https://pymodaq.readthedocs.io/en/stable/?badge=latest
   :alt: Documentation Status

.. image:: https://github.com/Attolab/pymodaq_plugins_stellarnet/workflows/Upload%20Python%20Package/badge.svg
    :target: https://github.com/Attolab/pymodaq_plugins_stellarnet

Custom PyMoDAQ Plugin to use StellarNet spectrometers in PyMoDAQ.

This plugin works now with modern python pyusb versions.


Authors
=======

* Romain Geneaux

Contributors
============


Instruments
===========

Below is the list of instruments included in this plugin

Viewer1D
++++++++

* **Stellarnet**: USB spectrometers made by StellarNet, Inc (https://www.stellarnet.us/spectrometers/).

Other Infos
===========

Capabilities
++++++++++++
- Basic measurement of spectra
- Setting for integration time
- Setting for "X Timing Rate" (unsure what it means but is present in constructor library)
- Smoothing of data with moving average (number of pixels of window can be changed)
- Averaging of data (actually only software averaging, so this could be removed as it is already present in basic PyMoDAQ functionalities) 
- Possibility of taking a snapshot of current spectrum which remains on display along with measurement. Useful to keep a reference or comparing two situations direclty in the lab. (notes: (1) snapshot can be cleared with "clear snapshot". (2) I did not check if/how the snapshot is saved when doing scans - better to just clear the snapshot before scanning).
- Possibility of using a calibration file for the absolute irradiance in W/m^2 (as provided by constructor for each specific spectrometer - typically needs to be requested upon purchase).

Installation notes
++++++++++++++++++
On windows, the installation of appropriate drivers working with pyusb can be fidly. I had most success using Zadig (https://zadig.akeo.ie/) to update the spectrometer drivers. Sadly if you change the drivers to work with python, the software provided by StellarNet will not work anymore. Hopefully the PyMoDAQ plugin works well enough so that you won't need the constructor software anymore :-)

Tested on Windows 10 with the driver WinUSB (v6.1.7600.16385).
