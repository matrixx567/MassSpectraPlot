Using the script
========================================================================================================================

The ``MassSpectraPlot.py`` script contains three different examples (see :ref:`Screenshots`) for plotting a mass
spectrum.


Exporting the raw data from the mass spectra software
------------------------------------------------------------------------------------------------------------------------

Every plot of a mass spectrum uses a ASCII based file with x/y data as inputs. This file must have the ending ``*.xy``.
An example of an input file can be found in the ``examples/inputs`` folder (`Github examples folder`_).
The x and y values are divided by a space character.

For example the input data for the spectrum can be exported from Bruker Daltonics DataAnalysis.
Using ``File -> Export -> Mass Spectrum -> Save as simple x-y ASCII File (*.xy)`` in the software to generate the
appropriate file.


Generating the peak label list
------------------------------------------------------------------------------------------------------------------------

The automatic annotation of peaks, described in the next section, uses an additional input file. This file must have the
same filename as the corresponding xy-file. The ending of the filename is ``*.txt``. E.g., ``substance1.txt`` contains
the peak labels for the spectra in ``substance1.xy``.

This file is a comma-separated file with two colons. The first value is the x-value of the peak to be annotated and the
second colon contains the label for the peak.

An example of this file can be found in ``examples/inputs`` (`Github examples folder`_).


Automatic annotate the peaks
------------------------------------------------------------------------------------------------------------------------



tbd.


Manually annotate peaks
------------------------------------------------------------------------------------------------------------------------

tbd.


Manually annotate distances between peaks
------------------------------------------------------------------------------------------------------------------------


Customize the plots
------------------------------------------------------------------------------------------------------------------------


.. _GitHub examples folder: https://github.com/matrixx567/MassSpectraPlot/tree/master/examples