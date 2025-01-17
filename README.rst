********
Lightway
********

Analysis and quality assurance/control pipeline for the NSLSII Inner-Shell Spectroscopy beamline.

`This <https://gist.github.com/danielballan/cd787e98bd0a2821b5f71932e22e460f>`_ is a great resource for creating a testing environment for tiled. `This <https://gist.github.com/danielballan/ebee67b3169e5c9e30a6230fc2ef21e1>`_ is one where data can be persisted.

Important notes
---------------

The default ``config.yml`` file can be found in ``deploy/local``. This file expects the user to know a few things by default:

*None of the data will be saved to disk*! By default, the config uses a mock MongoDB adapter which works in memory only.

The environment variable ``TILED_SINGLE_USER_API_KEY`` should be set and used in the client. Alternatively, one can manually set the single user API key:

.. code::

    authentication:
        single_user_api_key: my1api2key


The environment variable ``TILED_CONFIG`` should be set and point to the ``config.yml`` file of choice. This will allow you to serve the Tiled instance using a simple command: ``tiled serve config`` (Tiled will look for this environment variable and use that as the default path, instead of the user being required to provide one).

Funding acknowledgement
-----------------------

This research is based upon work supported by the U.S. Department of Energy, Office of Science, Office Basic Energy Sciences, under Award Number FWP PS-030. This research used resources of the Center for Functional Nanomaterials (CFN), which is a U.S. Department of Energy Office of Science User Facility, at Brookhaven National Laboratory under Contract No. DE-SC0012704.

Disclaimer
^^^^^^^^^^

The Software resulted from work developed under a U.S. Government Contract No. DE-SC0012704 and are subject to the following terms: the U.S. Government is granted for itself and others acting on its behalf a paid-up, nonexclusive, irrevocable worldwide license in this computer software and data to reproduce, prepare derivative works, and perform publicly and display publicly.

THE SOFTWARE IS SUPPLIED "AS IS" WITHOUT WARRANTY OF ANY KIND. THE UNITED STATES, THE UNITED STATES DEPARTMENT OF ENERGY, AND THEIR EMPLOYEES: (1) DISCLAIM ANY WARRANTIES, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE OR NON-INFRINGEMENT, (2) DO NOT ASSUME ANY LEGAL LIABILITY OR RESPONSIBILITY FOR THE ACCURACY, COMPLETENESS, OR USEFULNESS OF THE SOFTWARE, (3) DO NOT REPRESENT THAT USE OF THE SOFTWARE WOULD NOT INFRINGE PRIVATELY OWNED RIGHTS, (4) DO NOT WARRANT THAT THE SOFTWARE WILL FUNCTION UNINTERRUPTED, THAT IT IS ERROR-FREE OR THAT ANY ERRORS WILL BE CORRECTED.

IN NO EVENT SHALL THE UNITED STATES, THE UNITED STATES DEPARTMENT OF ENERGY, OR THEIR EMPLOYEES BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, CONSEQUENTIAL, SPECIAL OR PUNITIVE DAMAGES OF ANY KIND OR NATURE RESULTING FROM EXERCISE OF THIS LICENSE AGREEMENT OR THE USE OF THE SOFTWARE.
