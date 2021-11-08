# Notes


## The difference between the L1C and L2A products:
*L1C products provide the top of atmosphere reflectances in fixed cartographic geometry. Images are tiles of 100 sq. km and the products contain applied radiometric and geometric corrections.
*L2A products provide bottom of atmosphere reflectances in cartographic geometry. This product is currently processed by ESA using a processor running Sentinel-2 Toolbox.

## BOA vs TOA
 *The TOA reflectance values represent the "raw" reflectance of the Earth as measured from space. This is a mix of light reflected off the surface of the Earth and off the atmosphere. BOA in turn represents the actual reflectance of the areas on the surface of the Earth. The BOA values are calculated from the TOA values by using a physical model (Sen2Cor tool for Sentinel-2), with an attempt to eliminate the effect of the atmosphere on the reflectance values.
 
 *NDVI(BOA) is greater than NDVI(TOA) except for the smallest values of NDVI. This is due to the fact that the atmosphere is "blue", that is, the effect of the atmosphere is greatest in the short wavelengths of the electromagnetic spectrum. Moreover, near infrared reflectance is less affected by the atmosphere than visible light. Basically the atmospheric correction decreases the red reflectance more than the NIR reflectance and this explains the increase in the NDVI values, as can be seen by studying the original NDVI formula.
