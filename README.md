# dustmaps_guo2021
Based on the multi-band photometry of SkyMapper Southern Survey, Gaia DR2, the Two Micron All Sky Survey and the Wide-Field Infrared Survey Explorer Survey, we have estimated values of the r-band extinction for∼ 19 million stars with the spectral energy distribution (SED) analysis. Combined with the distances from the Gaia DR2 parallaxes, we have constructed a three-dimensional extinction map of the southern sky. The paper has been published by ApJ: https://ui.adsabs.harvard.edu/abs/2021ApJ...906...47G/abstract. This repository shows how to download the data underlying the article and how to use our 3D extinction maps.

### Southern-sky 3D extinction maps
The file 'guo2021.fits' is the full data of our 3D extinction maps of the southern sky. Each row of the file contains the extinction profile for one line of sight: Galactic coordinates l, b along with the extinction values at the individual distances E(B-V)_{0.2 kpc}, E(B-V)_{0.4 kpc}, E(B-V)_{0.6 kpc} ... E(B-V)_{5.8 kpc}, E(B-V)_{6.0 kpc} and respective uncertainties.

### All-sky 3D extinction maps
The file 'allsky2021.fits' is an all-sky extinction maps, which combine our 3D extinction maps in the southern sky and those from the literature. Similar as the 3D extinction maps in the souther sky, the file contains a table. Each row of the table contains the extinction profile for one line of sight: Galactic coordinates l, b along with the reddening values at the individual distances E(B-V)_{0.2 kpc}, E(B-V)_{0.4 kpc}, E(B-V)_{0.6 kpc} ... E(B-V)_{5.8 kpc}, E(B-V)_{6.0 kpc}.

If you have any questions or need more informations, please send emall to Bingqiu Chen (bchen@ynu.edu.cn) and Helong Guo (helong_guo@mail.ynu.edu.cn).
