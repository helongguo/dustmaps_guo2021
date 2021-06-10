# dustmaps_guo2021
Based on the multi-band photometry of SkyMapper Southern Survey, Gaia DR2, the Two Micron All Sky Survey and the Wide-Field Infrared Survey Explorer Survey, we have estimated values of the r-band extinction for∼ 19 million stars with the spectral energy distribution (SED) analysis. Combined with the distances from the Gaia DR2 parallaxes, we have constructed a three-dimensional extinction map of the southern sky. The paper has been published by ApJ: https://ui.adsabs.harvard.edu/abs/2021ApJ...906...47G/abstract. This repository shows how to download the data underlying the article and how to use our 3D extinction maps.

### Southern-sky 3D extinction maps
The file 'guo2021.fits' is the full data of our 3D extinction maps of the southern sky. Each row of the file contains the extinction profile for one line of sight: Galactic coordinates l, b along with the extinction values at the individual distances E(B-V)_{0.2 kpc}, E(B-V)_{0.4 kpc}, E(B-V)_{0.6 kpc} ... E(B-V)_{5.8 kpc}, E(B-V)_{6.0 kpc} and respective uncertainties.

    >>> from dustmaps.guo2021 import Guo2021SQuery
    
### All-sky 3D extinction maps
The file 'allsky2021.fits' is an all-sky extinction maps, which combine our 3D extinction maps in the southern sky and those from the literature. Similar as the 3D extinction maps in the souther sky, the file contains a table. Each row of the table contains the extinction profile for one line of sight: Galactic coordinates l, b along with the reddening values at the individual distances E(B-V)_{0.2 kpc}, E(B-V)_{0.4 kpc}, E(B-V)_{0.6 kpc} ... E(B-V)_{5.8 kpc}, E(B-V)_{6.0 kpc}.

    >>> from dustmaps.guo2021 import Guo2021AQuery
--------------------------------------------------------------------------------
If you have any questions or need more informations, please send emall to Bingqiu Chen (bchen@ynu.edu.cn) and Helong Guo (helong_guo@mail.ynu.edu.cn).

# dustmaps_chen2013
J/A+A/550/A42       Extinction map towards the Galactic bulge  (Chen+, 2013)

Three dimensional interstellar extinction map towards the Galactic bulge.
    Chen B., Schultheis M., Jiang B., Gonzalez O.A., Robin A.C., Rejkuba M.,
    Minniti D.
   <Astron. Astrophys. 550, A42 (2013)>
   =2013A&A...550A..42C

ADC_Keywords: Extinction ; Photometry, infrared ; Milky Way
Keywords: dust, extinction - Galaxy: bulge - Galaxy: stellar content -
          Galaxy: structure

Description:
    We combine the observations with the Besancon model of the Galaxy
    to investigate the variations of extinction along different lines of
    sight towards the inner Galactic bulge as a function of distance. The
    full results are listed in chen2013VVV.fits and chen2013GLIMPSE.fits. These results will be
    also added into the BEAM calculator webpage
    (http://mill.astro.puc.cl/BEAM/calculator.php). For each position we
    give the E(J-Ks), E(H-Ks) as well as the corresponding sigma for
    each distance bin starting from 1 to 10kpc.
  
To get the color excess e.g. E(H-Ks) based on the data from VVV

    from dustmaps.guo2021 import Chen2013VVVQuery    
    
To get the color excess e.g. E(K-3.6) based on the data from GLIMPSE

    from dustmaps.guo2021 import Chen2013GLIMPSEQuery       
 
    
For details on how to use this map, see the original paper:
    https://ui.adsabs.harvard.edu/abs/2013A%26A...550A..42C/abstract.

--------------------------------------------------------------------------------

Acknowledgements:
    Bingqiu Chen, bchen@ynu.edu.cn

# dustmaps_schultheis2013

We use data from the VISTA Variables in the Via Lactea survey together with the
Besancon stellar population synthesis model of the Galaxy to determine
interstellar extinction as a function of distance in the Galactic
bulge covering -10<l<10 and -10<b<5. We adopted a recently developed
method to calculate the colour excess. First we constructed the H-Ks
vs. Ks and J-Ks vs. Ks colour-magnitude diagrams based on the VVV
catalogues that matched 2MASS. Then, based on the temperature-colour
relation for M giants and the distance-colour relations, we derived
the extinction as a function of distance. The observed colours were
shifted to match the intrinsic colours in the Besancon model as a
function of distance iteratively. This created an extinction map with
three dimensions: two spatial and one distance dimension along each
line of sight towards the bulge. We present a 3D extinction map that
covers the whole VVV area with a resolution of 6'x6', for J-Ks and
H-Ks using distance bins of 0.5-1.0kpc. The high resolution and depth of
the photometry allows us to derive extinction maps for a range of
distances up to 10kpc and up to 30 magnitudes of extinction in AV
(3.0mag in AKs). Integrated maps show the same dust features and
consistent values as other 2D maps.

To get the color excess e.g. E(J-Ks) 

    from dustmaps.guo2021 import Schultheis2013Query

For details on how to use this map, see the original paper:
    https://ui.adsabs.harvard.edu/abs/2014A%26A...566A.120S/abstract.

--------------------------------------------------------------------------------

Acknowledgements:
       Mathias Schultheis, mathias.schultheis(at)oca.eu
# Conditions for using the program
The program relies on the dustmaps package. The dustmaps package provides a uniform interface for dealing with a number of 2D and 3D maps of interstellar dust reddening/extinction. For details and how to install, please refer to https://github.com/gregreen/dustmaps

