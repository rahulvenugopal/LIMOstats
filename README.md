# Learn LInear MOdeling of MEEG data
### Distance of neibouring electrodes
1. So, to define the spatial cluster we need to knwo for every electrode what are its neighbours
2. I am familier with `mne.channels.find_ch_adjacency` in mne-python. This function tries to infer the appropriate adjacency matrix template for the given channels. If a template is not found, the adjacency matrix is computed using Delaunay triangulation based on 2D sensor locations
3. Now, for my 64 channel montage, I gotta figure out what should be the neighbourdist
4. Documentation says
> For instance, 0.37 is a good distance for Biosemi standard 128 electrodes configuration. You can check the accuracy of neighbourdist for your electrode montage using the output neighbours
