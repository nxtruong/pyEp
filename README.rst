*******************
pyEp
*******************

Introduction
===============

pyEp is a python library that allows for the EnergyPlus ExternalInterface to be used in Python. Additionally, it provides an EnergyPlus-OPC bridge service that exposes EnergyPlus simulation variables as an OPC tree tag structure.

Key Components
===============
pyEp
""""""""""""""""""
ep_process is the base class, representing an EnergyPlus process. See example.py for an example of how to create and run a simulation.

EnergyPlus-OPC Bridge
"""""""""""""""""""""""
The EnergyPlus-OPC bridge is a process which presents EnergyPlus ExternalInterface tags as OPC tags in a Simulated Server. The Bridge works out of the box with the `MatrikonOPC Simulation Server  <https://www.matrikonopc.com/products/opc-desktop-tools/index.aspx>`_. Controlling the Bridge requires another process, a "controller" that determines which inputs to provide to EnergyPlus. Two controllers are included, an example controller which implements a fixed set point schedule in the Python code, and another which implements a fixed set point schedule from a csv file. 

Requirements
===============
The pyEp core module is compatible for 2.7 and 3.5. EnergyPlus versions 8.1 and 8.4 have been tested, although it is likely that it works with any 8.x version. The EnergyPlus-OPC Bridge uses OpenOPC and Pyro3 for communications and requires 2.7.
