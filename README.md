RSurvey: A processing program for spatially distributed data
============================================================

Description
-----------

This [R](http://www.r-project.org/ "R") package is a processing program for
spatially distributed data. It features graphing tools, query building, and
polygon clipping. A graphical user interface (GUI) is provided.

Files can be one of four types as indicated by their extension: tables
(_.txt_, _.csv_, _.dat_, or _.shp_), grids (_.grd_), polygons (_.ply_), or
project images (_.rda_). Tables (_.txt_, _.csv_, _.dat_) can be compressed
by [gzip](http://www.gzip.org/ "gzip") with additional extension _.gz_.
Shapefles (_.shp_) and interpolated grid files (_.grd_) are limited to data
export. Support for programmatic manipulation of measurement units is only
provided for date-time values; therefore, the bulk of unit consistency is tasked
to the user. Time zones, spatial datum's and projections are not supported.

The set of standards used for coding
[RSurvey](http://cran.r-project.org/web/packages/RSurvey/index.html "RSurvey")
is documented in
[Google's R Style Guide](http://google-styleguide.googlecode.com/svn/trunk/google-r-style.html "Google's R Style Guide").

Installation
------------

If R is not already installed on your
computer, download and install the latest binary distribution from
[CRAN](http://cran.r-project.org/ "The Comprehensive R Archive Network").
The GUI requires R operate as an SDI application, using multiple
top-level windows for the console, graphics, and pager.

Install the required R packages from CRAN using a simple call to
`install.packages()`:
    install.packages(c('tcltk', 'sp', 'gpclib', 'rgl', 'MBA', 'tripack', 'RSurvey'))

Exporting to shapefiles requires the R package
[rgdal](http://cran.r-project.org/web/packages/rgdal/index.html "rgdal"):
    install.packages('rgdal')

Support for displaying table data is provided by
[tktable](http://tktable.sourceforge.net/ "tktable"),
a spreadsheet-like [Tcl/Tk](http://www.tcl.tk/ "Tcl/Tk") widget
(included with the Windows binary distribution of R).
    tclRequire('Tktable', warn = TRUE)

Running
-------

Load RSurvey in the current R session:
    library(RSurvey)
Load a sample RSurvey project into the current R session (optional):
    data(project)
Activate the main GUI:
    OpenRSurvey()
