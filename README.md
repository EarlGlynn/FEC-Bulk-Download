# FEC Bulk Download

For many years the [Federal Election Commission](https://classic.fec.gov/finance/disclosure/ftpdet.shtml) provided an FTP server for bulk download of political contribution data for federal elections in the US.

Last year the FEC "moved" the files to an [Amazon-hosted cloud resource](https://cg-519a459a-0ea3-42c2-b7bc-fa1143481f74.s3-us-gov-west-1.amazonaws.com/bulk-downloads/index.html).  Anonymous FTP downloads no longer work, nor does the handy `wget` tool to download specific files or folders. The FEC acknowledged the problem on their [FEC GitHub page](https://github.com/fecgov/) in the article [Retrieving S3 bulk download files](https://github.com/fecgov/fec-cms/wiki/Retrieving-S3-bulk-download-files).

Now only the [Amazon command-line interface](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) can be used to transfer files, and Amazon is pushing the latest ["version 2" of these tools](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) as tool of choice.

The many changes over the last several years on the FEC site are not always easy to follow, so the notebooks in this repository show my attempts to download bulk data from the FEC bulk download site.

Jupyter notebooks:

* `FEC Bulk Download -- Getting Started.ipynb` shows how to access the FEC bulk download site, display lists of files, and download files.

* `FEC Bulk Download -- Make Local Copy.ipynb` shows how to download all files from the FEC Bulk Download site:  29,620 files, 61.8 GB (transferred in nearly 100 minutes elapsed time on 2019-11-29). File `FEC-Bulk-Download-List.txt` is a list of all 29,620 downloaded files.

Downloaded folders of interest:

* Folders 1978 .. 2024 have data by election cycle.  Folders 1980 .. 1998 have `Old Format` subfolders to preserve original data.  I think in recent years the files have all been converted to a unified format?  The `data_dictionaries` folder has info about file formats.

* Folder `electronic` has the daily ZIP files which expand into all the .fec files from dates 2001-02-01 through 2019-11-28.  See the `efile readme.txt` and the 100s of file formats documented in `eFilingFormats.zip`.

* Folder `paper` seems to have .fec files for certain paper submissions?

* Folder `data.fec.gov` has candidate disbursement data since 2010, along with leadership and lobbyist information.

Can anyone suggest better sources for historical or technical information about this FEC resource?
