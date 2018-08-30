# equiVolve
For IO and toy codes to handle Equinor's Open Domain Volve Dataset

To download large data files from https://data-equinor-com.azurewebsites.net/dataset/volve, save <i>download_file.py</i> into the directory in which you want to store your data. Then in a terminal window, run the following command within that directory:

<b>python download_file.py</b> 

<br>

You can control which file is downloaded by modifying the url entry near the top of file. In addition, you may change the <i>chunk_size</i> input within the function <i>download_file(url, chunk_size = 2**30)</i> to what you deem is necessary. The default is set to download the 2.6 TB file <i>Seismic.ST10010.zip</i>, at a chunk size of 1 GB. It has been verified to work on Python 3.6.

Please look at <i>ST10010_file_list.txt</i> before you decide to download this file and verify this is the data you want. The file unzip'd totals 3.3 TB, which means that <b>you will need at minimum 6 TB</b> to manage this one dataset for both the download and the extraction. If you only need a select file from the archive, you can use <i>unzip -l Seismic.ST10010.zip filename</i> or <i>unzip -l Seismic.ST10010.zip directory_name</i> to extract a particular filename or directory and minimize the amount of space you need.

<i>download_file.py</i> can resume a download if the download is cut for whatever reason. Just re-run the above command and it will resume from the appropriate byte position. If you have a problem with the download being interrupted too often, you may wish to use a wrapper file to run the script until the full file is downloaded.

The Volve dataset is open domain and can be accessed via this script on networks outside of Equinor. 

<br>

### md5 checksums
Seismic.ST10010.zip: 6fd57d14cd716f52a8df0088d9831f88

Reports_Volve.zip: 7a5f4c862d5b1005572810905bfee6a3
