# ATA Beamformer 2 Filterbank

This program converts raw beamformer time domain data from the Allen Telescope Array into the Filterbank format. The filterbank file will contain data in the frequency domain.

Code used to learn about the Filterbank header creation:

https://github.com/UCBerkeleySETI/gbt_seti/blob/master/src/filterbank_mkheader.c

Section 3 of sigproc.pdf explains about the Filterbank format:

http://sigproc.sourceforge.net/sigproc.pdf

Example:

./bf2fb -h prints the help and exits.

This will read in the raw beamformer data and create a file names test.bin with 10 seconf interation times:

./bf2fb -input ../../anttest10_1ants_w3oh_6660_4hrphase.raw -outfreq 1422.5 -outbw 0.1 -fftsize 128 -int 10000 -output ./testdata/test.fil -source w3oh

sudo ./bf2fb -input /data/psrB0329+54-2990mhz-april22-2018.raw -outfreq 2990 -outbw 0.1 -fftsize 1024 -int 64 -output /data/ptest1.raw -source ptest1

Note: this is a work in progress. The -outfreq and -outbw do nothing yet.





