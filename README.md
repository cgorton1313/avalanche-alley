# avalanche-alley

## Project Structure

**/raw_data**

*This folder is for original, unmodified data. Each subfolder refers to the source.*

/raw_data/aa
*Avalanche Alley program data*
data_obs_avy.csv - table of all program avalanche observations

/raw_data/nws
*National Weather Service Data*
This folder contains html files downloaded from the National Weather Service. The API did not have all the data we wanted, so we opted for html pages that can be scraped by our scripts.

Note: each file includes several hours of data that are not part of the indicated year. This is due to the website's inability to deal with time zones. These hours must be cropped by the script!

nws-settings.png - screenshot of how to manually download the data. The script produces a direct link though.

/raw_data/sp
*SnowPilot Data*
These are xml files of snow profiles (aka snow pits), as downloaded from SnowPilot.

The Snow Pilot xml schema has been replaced by caaml, but that is much more difficult to parse so we're keeping it simple.

all_MT.xml - all the snow profile data that exists from Montana.

**/data_prep**

*This folder is for handling the raw data. Any scripts and their output are stored here.*

/data_prep/pkl
*The output of data prep scripts should be placed here. These pickles should be ready for an analysis script to ingest.*

## Data Dictionary

### avtype
L Loose-snow avalanche
WL Wet loose-snow avalanche
SS Soft slab avalanche
HS Hard slab avalanche
WS Wet slab avalanche
I Ice fall or avalanche
SF Slush flow
C Cornice fall (w/o additional avalanche)
R Roof avalanche
U Unknown

### avtrigger
NATURAL OR SPONTANEOUS
N Natural trigger
NC Cornice fall
NE Earthquake
NI Ice fall

NL Avalanche triggered by loose snow ava-
lanche (Figure 3.4)

NS Avalanche triggered by slab avalanche
NR Rock fall
NO Unclassified natural trigger (specify

in comments)
ARTIFICIAL TRIGGERS: EXPLOSIVE
AA Artillery
AE An explosive thrown or placed on or
under the snow surface by hand

AL Avalauncher
AB An explosive detonated above the

snow surface (air blast)

AC Cornice fall triggered by human or

explosive action
AX Gas exploder
AH Explosives placed via helicopter

AP Pre-placed, remotely detonated explo-
sive charge

ARTIFICIAL TRIGGERS: MISCELLANEOUS
AW Wildlife
AU Unknown artificial trigger
AO Unclassified artificial