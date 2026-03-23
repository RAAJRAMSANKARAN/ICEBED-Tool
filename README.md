**ICEBED: ICe volumE and Bedtopography Estimation from DEM**<br>
<br>
**Overview**<br>
  ICEBED is a software tool that helps estimate glacier ice thickness, ice volume, and ice bed topography. This tool features a user-friendly GUI, enabling users to estimate the required outputs for one or multiple glaciers by following simple steps. ICEBED is a **fully automated, stand-alone tool, coded in MATLAB**. It requires three primary inputs to estimate spatially distributed ice thickness: ***Digital Elevation Model (DEM)***, ***surface slope***, and ***glacier mask***.<br>
  <br>
**Model Framework**<br>
  The ICEBED tool **automates** the ***GlabTop2_IITBversion ice thickness model*** (refer to *Ramsankaran et al., 2018*), an independently implemented version of the GlabTop2 model developed by *Frey et al. (2014)*.
Both GlabTop2 and the GlabTop2_IITB version are based on the same model formulation and follow identical modelling principles; the differences lie only in their implementation.<br>
1. *Input structure*: GlabTop2 uses DEM and glacier boundary as inputs, whereas the GlabTop2_IITB version requires DEM,     glacier mask, and pre-computed surface slope.
2. *Processing approach*: GlabTop2 utilises IDL-based functions, whereas the GlabTop2_IITB version uses MATLAB routines with a buffer-based method for mean slope estimation.
3. *Interpolation scheme*: GlabTop2 applies basic IDW interpolation, while the GlabTop2_IITB version uses a modified IDW approach with an adjusted distance weighting exponent.<br>

Overall, the *GlabTop2_IITB version offers greater control over inputs and processing steps, resulting in a more flexible and robust implementation*.<br>
  <br>
**Outputs and Shape Factor Handling**<br>
  ICEBED provides spatially distributed estimates of ice thickness and corresponding bed topography for the selected glacier(s). In addition, the tool generates ice thickness outputs for shape factor values ranging from 0.6 to 0.9 at increments of 0.01 (30 scenarios). The tool also computes, by default, an averaged ice thickness dataset from these 30 estimates, which is required for shape factor optimisation.<br><br>
  For standard applications, users may directly use the ice thickness corresponding to a shape factor of 0.8 or any other value. Alternatively, users may manually derive an optimised shape factor following Ramsankaran et al. (2018), where the averaged ice thickness is used as an input. The optimised shape factor value then allows selection of the corresponding ice thickness as the final estimate. <br>
  <br>
**Documentation**: Details of executing the ICEBED tool can be found in the instruction manual ***'ICEBED_Tool_Instructions_V3'***.<br>
<br>
**Download ICEBED tool** [here](https://github.com/RAAJRAMSANKARAN/ICEBED-Tool-/releases)
