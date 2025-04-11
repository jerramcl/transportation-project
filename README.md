# Investments in Public Transportation on Property Value in Alameda County  
<p align="center">
  <img src="https://github.com/user-attachments/assets/c500a672-8b94-4ace-b865-cd36575424c8" alt="Bay-Area-Rapid-Transit-logo" width="300"/>
</p>
This project explores whether the expansion of Bay Area Rapid Transit (BART) to Warm Springs in Fremont, CA led to an increase in nearby property values. Previous research suggests that public transit investments often generate long-term economic value. My analysis tested this assumption empirically using an econometric approach. 

I built a Weighted Least Squares (WLS) regression model using monthly, inflation-adjusted Zillow Home Value Index (ZHVI) data from 2011 to 2020 for the two zip codes closest to the station (94538 and 94539). My model included controls for mortgage rates, unemployment, lagged property values, and featured a binary interaction term to capture the effect of the station’s 2017 opening. I addressed serial correlation with clustered standard errors and corrected for heteroskedasticity by weighting based on the residual variance from an initial OLS model.

The interaction coefficient was slightly negative (-0.0584), but **not statistically significant (p = 0.201)**, meaning I failed to reject the null hypothesis. In other words, **the opening of the Warm Springs Transit Center did not have a significant effect on nearby property values** during the post-treatment period. However, I found that macroeconomic indicators, like mortgage and unemployment rates, were significant predictors: a **1% increase in mortgage rates was associated with a 10% decrease in home values, and a 1% increase in unemployment led to a 4% decrease.** 

A key limitation of the analysis was the use of zip-code level data, which may have masked more localized effects within a smaller radius of the station. Having access to more granular data would have made this analysis more robust. I considered more advanced methods like Difference-in-Differences and Instrumental Variable (IV) models, but found they were not suitable given data constraints and violated assumptions. For example, announcements about the station may have influenced property values years before construction began, and I lacked a strong instrument for IV analysis.

While I didn’t find a significant impact on property values, this doesn’t discount the broader public benefits of transit investments—such as reducing traffic congestion, improving air quality, and increasing access to jobs. This project highlights the importance of access to more granular, property-level data, and suggests that future research should incorporate additional variables like commercial development, zoning changes, and specific transit-oriented housing policies (e.g., [SB-167](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=201720180SB167)). Ultimately, this case study serves as an example of how careful empirical design can shed light on complex policy questions, even when the results challenge conventional assumptions.







Note: see code in the .ipynb linked above, and data in the csv file
