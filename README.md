# A-Hierarchical-Decision-Framework-for-LCS-Deployment-in-Lake-Monitoring-under-Uncertainty
Data and codes for LCS deployment in lake monitoring under uncertianty
This repository provides the workflow and scripts used for the hierarchical deployment of low-cost sensors under uncertainty.

1. Data preprocessing
Raw monitoring data are provided in Raw data.xlsx, including coordinates and observed water quality variables. These data are interpolated to generate a continuous spatial field, which serves as the reference (error-free) field.

2. Error field generation
Measurement uncertainty is simulated by adding synthetic errors to selected sampling points using Monte Carlo simulations (50, 100, 200, 400, and 500 realizations). Errors are generated according to the predefined error grades described in the paper. The uncertainty stability is evaluated using the RSD of 32 existing monitoring sites.

3. Quality–quantity screening (MI–CI analysis)
Mutual Information (MI) and its confidence interval (CI) are computed across candidate sampling densities to identify an information-efficient deployment range under uncertainty.

4. Spatial cluster identification
High–High (HH) and Low–Low (LL) clusters are identified using the LISA method implemented in ArcGIS, based on the simulated error fields.

5. Hierarchical site selection
Value of Information (VOI) and complex network metrics are calculated for candidate sites.
The resulting indicators are used as inputs to HierachicalSelection.m to generate the final hierarchical deployment order.

6. Performance evaluation
The selected deployment configurations are evaluated using hotspot identification and coverage metrics described in the manuscript.
