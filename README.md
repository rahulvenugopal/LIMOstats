# Learn LInear MOdeling of MEEG data
### Distance of neibouring electrodes
1. So, to define the spatial cluster we need to know for every electrode what are its neighbours
2. I am familiar with `mne.channels.find_ch_adjacency` in mne-python. This function tries to infer the appropriate adjacency matrix template for the given channels. If a template is not found, the adjacency matrix is computed using Delaunay triangulation based on 2D sensor locations
3. Now, for my 64 channel montage, I gotta figure out what should be the neighbourdist
4. Documentation says
> For instance, 0.37 is a good distance for Biosemi standard 128 electrodes configuration. You can check the accuracy of neighbourdist for your electrode montage using the output neighbours
5. `accs_elecneighbours` uses Euclidan distances and for my chanlc, the maximum distance was 2 and minimum 0
6. Have to look at each electrode's neighbours and contrast with what [fieldtrip syas](https://www.fieldtriptoolbox.org/example/neighbours/) to finalise the cut-off distance
