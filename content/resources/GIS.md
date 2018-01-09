+++
type = "resources"
author = "Doug Goodwin"
date = "2017-06-22"
title = "Metro Bus & Rail GIS Data"
description = "Metro’s GIS data includes 2 types of line shapefile (Bus Lines and Rail Lines) and three types of point shapefile (Bus Stops, Rail Stations and Rail Portals)."
featured = ""
featuredpath = ""
featuredalt = ""
categories = ["DATA"]
linktitle = ""
format = ""
link = "#"
+++

## Metro Bus Line Shapefiles

The Metro Bus Line Zip File contains 5 shapefiles that cover all Metro Bus Lines. A shapefile is a set of 3 to 7 interrelated files that can be used with mapping (GIS) software. These technical files that have no other application; you must have GIS software to use them. The shapefiles are redrawn every six months, typically in June and December. We’ll try to post them within six weeks of changes.

The 5 shapefiles each contain a group of Metro Bus Lines. The 5 groups are:

1. LocalCBDmmyy: Metro Local Lines that go through Downtown Los Angeles (Lines 2 through 96).
2. LocalNonCBDmmyy: Metro Local Lines that do not go through Downtown Los Angeles (Lines 102 through 292).
3. LimExpmmyy: Metro Limited or Express Lines (Lines 344 through 577 and 788).
4. ComCircmmyy: Metro Community Circulator Lines (Lines 603 through 687).
5. RapidBRTmmyy: Metro Rapid Lines and the Orange Line (Lines 704 through 794, except Line 788, and Lines 901 through 910).

(Note: “mmyy” stands for the month and year of the shakeup.)

The bus line shapefiles are generated from basic operating schedules for all trunk lines. Branch lines and short-lines are subsets of these lines. Example: Only Limited Line 344 is listed under Lim&Exp. The other Limited Routes (i.e., routes that skip stops) are branch lines that will be found under their parent trunk line (e.g., Limited Line 302 is a branch of Local Line 2).

The attribute file (dbf) of any bus line shapefile has a column, “Var_Route” which identifies the Trunk Line. A trunk line may have many rows associated with this Line. Each of these represent a trip pattern that may be assigned to a bus.

The attribute file also contains a column “Var_Descr” that further describes the trip pattern. A bus route that differs from the trunk line’s route (enough to be given its own Route number in the bus’ headsign) will be indicated in this column. In order to have a single bus line displayed on a map use your GIS software to highlight and/or export the trip patterns with that bus line’s name.

## Metro Bus Stop Shapefiles

Similar to the Metro Bus Line shapefiles, the Bus Stop shapefile is a set of interrelated files that can be used with GIS software.  Two Bus Stop shapefiles are available, each with the same content but organized differently. These shapefiles will be updated every shakeup in tandem with the Bus Line shapefiles.

Bus Lines and Bus Stops are really separate systems on a map.  While the bus line shapefiles are snapped to the street centerline, the bus stops are the exact points where the stops occupy the sidewalk; they are necessarily offset from the lines.

## Metro Rail Line Shapefiles

The Metro Rail Line shapefiles show the Route of Line (ROW) of each Rail Line.  These are not revised per shakeup because the ROW does not change.  The overall Rail Line zip file will be amended as new lines are added or existing lines are extended.

## Metro Rail Station Shapefiles

These are point shapefiles where the measurement point is center-platform.

## Metro Rail Portal Shapefiles

These are the entrances to each rail station. More than one portal may be listed at a station: any portal more than 50 feet from another has its own row in the dataset and will appear as a separate point location when mapped.