# mediaren

Rename single media file or all files in directory based on exif gps metadata.

Runs on bash/csh shell on Linux, MacOS or Windows WSL.

Uses:

- exiftool
- curl
- queries to ArcGIS

What does it actually do?

mediaren will look at the metadata of media files, and using the gps coordinates found and the earliest date available, will rename the media file:

from 'original_filename.ext'
to 'yyyymmdd - location_in_english original_filename.ext'

Exception: if the process finds that the prefix is already a date in the format yyyymmdd, then it will rename the media file:

from 'original_prefix original_filename.ext'
to 'original_prefix - location_in_english original_filename.ext'


Note: ArcGIS has a limit of 3,000 queries per day for free use.

