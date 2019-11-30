# FEC Bulk Download

For many years the [Federal Election Commission](https://classic.fec.gov/finance/disclosure/ftpdet.shtml) provided an FTP server for bulk download of political contribution data for federal elections in the US.

Last year the FEC "moved" the files to an Amazon-hosted cloud resource.  Anonymous FTP downloads no longer work, nor does the handy `wget` tool to download specific files or folders.

Now only the Amazon command-line interface can be used to transfer the files, and Amazon is pushing the lastest ["version 2" of these tools](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) as tool of choice.

The many changes over the last several years on the FEC site are not always easy to follow, so the notebooks in this repository show my attempts to download bulk data from the FEC bulk download site.

Jupyter notebooks:

* `FEC Bulk Download -- Getting Started.ipynb` shows how to access the FEC bulk download site, display lists of files, and download files.

