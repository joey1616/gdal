.. _pct2rgb:

================================================================================
pct2rgb
================================================================================

.. only:: html

    Convert an 8bit paletted image to 24bit RGB.

.. Index:: pct2rgb

Synopsis
--------

.. code-block::

    pct2rgb [--help] [--help-general]
               [-of format] [-b band] [-rgba] [-pct palette_file] <source_file> <dest_file>

Description
-----------

This utility will convert a pseudo-color band on the input file into an output
RGB file of the desired format.

.. note::

    pct2rgb is a Python utility, and is only available if GDAL Python bindings are available.

.. program:: pct2rgb

.. include:: options/help_and_help_general.rst

.. option:: -of <format>

    Select the output format. Starting with
    GDAL 2.3, if not specified, the format is guessed from the extension (previously
    was GTiff). Use the short format name.

.. option:: -b <band>

    Band to convert to RGB, defaults to 1.

.. option:: -rgba

    Generate a RGBA file (instead of a RGB file by default).

.. option:: -pct <palette_file>

    Extract the color table from <palette_file> instead of getting it from <source_file>.
    Can be used to have a consistent color table for multiple files.
    The <palette_file> must be either a raster file in a GDAL supported format with a palette
    or a color file in a supported format (txt, qml, qlr).

.. option:: <source_file>

    The input file.

.. option:: <dest_file>

    The output RGB file that will be created.

The '-expand rgb|rgba' option of :ref:`gdal_translate` obsoletes that utility.
