# Python-Project-3E
Scientific Question:

DNA is tightly wound into nucleosomes in cells. This act is energy intensive, especially for DNA sequences that are structurally or energetically unfavorable. It is known that there is no "nucleosome positioning code" for humans; we can not accurately predict nucleosome sites in our DNA. My scientific question is whether this is the case for other organisms. Specifically, do smaller and less complex organisms show more sequence-driven nucleosome positioning? Single-celled organisms have to balance energy consumption for all life-sustaining processes throughout the cell. On the other hand, multicellular organisms such as humans have cells specialized for different tasks; it seems reasonable to postulate that our genome organization is not as streamlined as it is for single-celled organisms.

Upon searching through the literature, I have decided to analyze nucleosome maps produced through chemical mapping rather than through MNase cleavage, the reason being that chemical mapping produces greater accuracy and can identify 'fragile nucleosomes' that are lost in MNase digestion. This leaves me with a narrow choice of datasets as chemical mapping is harder to perform then MNase mapping. Therefore, I chose fission yeast as a representive for single-celled organisms and mouse ESCs for the multicellular counterpart, as I could not find a dataset for chemical nucleosome mapping in human cells.


Scientific Hypothesis:

Nucleosome positions show stronger sequence preferences in yeast compared to mouse ESCs. 

To test my hypothesis, I downloaded nucleosome maps characterized in: 
Moyle-Heyrman, G. et al.(2013) Chemical map of Schizosaccharomyces pombe reveals species-specific features in nucleosome positioning. PNAS110(50)20158-20163; DOI: 10.1073/pnas.1315809110 
Voong, L.N. et al.(2016) Insights into Nucleosome Organization in Mouse Embryonic Stem Cells through Chemical Mapping. Cell 167(6)P1555-1570.E15; DOI:https://doi.org/10.1016/j.cell.2016.10.04911/30/2020 

The nucleosome maps were downloaded from GEO. In order to map the DNA surrounding the nucleosomes, the genomes for both organisms were downloaded, yeast from GEO records and mouse from NCBI (the code for downloading the mouse genome can be found in another file; due to file size restrictions, the mouse genome and associated nucleosome coordinates are not included in the repository) To characterize the sequences surrounding nucleosomes, I scanned for dimer frequency through a manually written code and produced position-weight-matrices for the nucleosome 'motif' using biopython. However, I incorrectly used the mm39 mouse genome instead of the mm10 genome used by the authors in the ESC paper. Due to time and hardware constraints, I went ahead with the analyses. The pwm for mouse nucleosomes was produced using only a subset of all mouse nucleosomes, again due to the same limitations.
