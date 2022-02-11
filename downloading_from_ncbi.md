### Downloading GORG-Tropics SAG assemblies from NCBI
I had trouble finding a command line approach to do download all SAG assemblies from NCBI.  

Best attempt is to do it manually via the ncbi website...

First, go to bioproject for GORG: https://www.ncbi.nlm.nih.gov/bioproject/PRJEB33281

Then click 'Assembly' in 'Related Information' panel on right side of webpage.  All the assemblies can then be downloaded by clicking 'Download Assemblies'

If we want specific SAGs from these assemblies, we can run a search for them.  For example, I wanted just assemblies from plate 'AG-910', so I ran a search as such:
'AG-910* AND PRJEB33281'

### Downloading a sra fastq file, and subsampling:  
this one subsamples 300000 reads  
```
fastq-dump --split-files --skip-technical -N 0 -X 300000 --gzip --readids SRR6507279
```
