Operation
=========

Set-up
------

Parameter files
^^^^^^^^^^^^^^^
Three parameter files are used to control GLOBSIM. There is one for each step (download, interpolate, scale).


Downloading
--------------
**project_directory** - 

**credentials_directory** - The location of the credential files `.merrarc` and `.jrarc`.  Does not apply to credential file .ecmwfapi which defaults to your home directory. It is recommended to set this parameter to your home directory

**chunk_size** - How many days to include in each download file.  Larger chunk size values mean that a smaller number of files will be downloaded, each with a larger size

**bbN** - coordinates for northern boundary of bounding box describing the area for which data will be downloaded.  Coordinates must be in decimal degrees.

**bbS** - coordinates for southern boundary of bounding box describing the area for which data will be downloaded. Coordinates must be in decimal degrees.

**bbW** - coordinates for western boundary of bounding box describing the area for which data will be downloaded.  Coordinates must be in decimal degrees with negative values for locations west of 0.

**bbE** - coordinates for eastern boundary of bounding box describing the area for which data will be downloaded. Coordinates must be in decimal degrees with negative values for locations west of 0.

**ele_min**
**ele_max**

**beg** - first date for which data is downloaded YYYY/MM/DD
**end** - last date for which data is downloaded YYYY/MM/DD

**variables** - which variables should be downloaded from the server. The variables names come from the `CF Standard Names table <http://cfconventions.org/Data/cf-standard-names/59/build/cf-standard-name-table.html>`_.  It is recommended that the variables parameter be left to include all relevant variables: air_temperature, relative_humidity, precipitation_amount, downwelling_longwave_flux_in_air, downwelling_longwave_flux_in_air_assuming_clear_sky, downwelling_shortwave_flux_in_air, downwelling_shortwave_flux_in_air_assuming_clear_sky,  wind_from_direction, wind_speed




Interpolating
-------------
**project_directory** - 

**station_list** - 

**list_name** - 

**chunk_size** - How many time-steps to interpolate at once. This helps memory management. Keep small for large area files and/or computers with little memory. Make larger to get performance improvements on computers with lots of memory.

**beg** - beginning of date range for which data will be interpolated in YYYY/MM/DD format.  Note that this date range must include dates that are represented in the downloaded data.

**end** - end of date range for which data will be interpolated in YYYY/MM/DD format.  Note that this date range must include dates that are represented in the downloaded data.

**variables to interpolate** - which variables should be downloaded from the server. The variables names come from the `CF Standard Names table <http://cfconventions.org/Data/cf-standard-names/59/build/cf-standard-name-table.html>`_.  It is recommended that the variables parameter be left to include all relevant variables: 

Rescaling
---------
**project_directory** - 

**output_file** - path to output netCDF to be created. 

**overwrite** - Either *True* or *False*. Whether or not to overwrite the `output_file` if it exists.

**time_step** - how frequently should the output be written

**kernels** - which processing kernels should be used. Missing or misspelled kernels will be ignored by globsim.


