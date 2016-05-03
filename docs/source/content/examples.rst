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

An example for automic generation of the labels is shown in method
``generate_massspectra_plot_automatic_labels(input_filename, output_filename)``.

The function will read the raw values and the label values from the input files. After that the function will generate
all labels with a definated minimum distance (``delta_x_text_labels_mm``) between the labels`.


Manually annotate peaks
------------------------------------------------------------------------------------------------------------------------

A peak can be annotated with the function ``annotate_point``. Therefore the x value of the point and the horizontal 
position of the label have to be given. By using the ``raw_values`` dataframe the function searches the peak next to
the given ``x_value`` automatically.
 
The method ``generate_massspectra_plot_distance_peak_manual_annotation(input_filename, output_filename)`` shows the
usage of the explained function.


Manually annotate distances between peaks
------------------------------------------------------------------------------------------------------------------------

A distance between two peaks can be plotted by using the function ``annotate_distance``.


An example is shown in the function ``generate_massspectra_plot_distance_peak_manual_annotation(input_filename, output_filename)``.




Comparing two individual plots
------------------------------------------------------------------------------------------------------------------------

The function ``generate_massspectra_two_plot_manual_annotation(input_filename1, input_filename2, output_filename)``
plots two graphs vertically.

It is important to use the right raw_values data for annotating some peaks. 



Customize the plots
------------------------------------------------------------------------------------------------------------------------

The margins and dimensions of the plots are given in milimeter and can be easily customized.



.. _GitHub examples folder: https://github.com/matrixx567/MassSpectraPlot/tree/master/examples