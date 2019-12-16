# UNICEF-Arm-2030-Vision-1-Flood-Prediction-in-Malawi
ZINDI : UNICEF Arm 2030 Vision Flood Prediction in Malawi

# Context 
On 14 March 2019, tropical Cyclone Idai made landfall at the port of Beira, Mozambique, before moving across the region. Millions of people in Malawi, Mozambique and Zimbabwe have been affected by what is the worst natural disaster to hit southern Africa in at least two decades.

In recent decades, countries across Africa have experienced an increase in the frequency and severity of floods. Malawi has been hit with major floods in 2015 and again in 2019. In fact, between 1946 and 2013, floods accounted for 48% of major disasters in Malawi. The Lower Shire Valley in southern Malawi, bordering Mozambique, composed of Chikwawa and Nsanje Districts is the area most prone to flooding.

The objective of this challenge is to build a machine learning model that helps predict the location and extent of floods in southern Malawi.

This competition is sponsored by Arm and UNICEF as part of the 2030Vision initiative.

About 2030Vision (2030vision.com):


2030Vision is an initiative founded to propel technology forward to support the Sustainable Development Goals (SDGs). 2030Vision aims to transform the use of technology through collaborative partnerships and innovative projects, to support the delivery of the SDGs and unlock the commercial opportunities they offer, by identifying and scaling impactful technologies through multi-sector partnerships.

About UNICEF (unicef.org):


The United Nations Children's Fund (UNICEF) is a United Nations agency responsible for providing humanitarian and developmental aid to children around the world. UNICEF works in some of the world’s toughest places, to reach the world’s most disadvantaged children. Across more than 190 countries and territories, we work for every child, everywhere, to build a better world for everyone.

About Arm (arm.com):


Arm is the world’s leading semiconductor IP company with technologies reaching 70% of the global population. Arm’s device architectures orchestrate the performance of the technology that's transforming our lives — from smartphones to supercomputers, from medical instruments to agricultural sensors, and from base stations to servers. In response to the Global Goals and in recognition of Arm’s position within the technology sector, Arm founded 2030Vision in 2017, in partnership with the UN system and others.

# Data description 


Southern Malawi experienced major flooding in 2015 and again in 2019 with cyclone Idai. Approximate dates of impact are 13 January 2015 and 14 March 2019, respectively.

We have broken up the map of southern Malawi into approximately 1 km sq squares. Each square has a unique ID. Each square has been assigned a "target" value which is the fraction (percentage) of that square that was flooded in 2015.

For this competition, the training data is the flood extent in 2015 in southern Malawi, however, you are encouraged to source other flood data for other nearby regions and other historic floods to train your model. (Just be sure to propose any new datasets that are not listed here to Zindi at zindi@zindi.africa for approval.)

The test data to measure the accuracy of your model is the flood extent in southern Malawi in 2019.

Each unique square also has some additional features that we have already extracted for you. Although we encourage you to add more yourself, these features are included as a starting point. They are:

Elevation. Mean elevation over the square, based on this dataset in Google Earth Engine.
Dominant Land Cover Type. Most areas are predominantly grasslands, savannah or cropland. You can find the full list of land cover types here in the ‘LC_Type1 Class Table’.
Weekly Precipitation. Historical rainfall data for each square, for 18 weeks beginning 2 months before the flooding. Rainfall estimates from this dataset in Google Earth Engine.
Train.csv has the target variable for 2015, along with the above features (including rainfall for both the 2015 and 2019 flood events). The submission file should have the predicted target for 2019 and cover the same locations as Train. The X, Y coordinates given represent a sqaure 0.01 degrees on each side, centered on that X-Y location.

The target is the percentage of the given rectangle that was flooded, with a value between 0 and 1.

In addition to the features we have provided in the train and test CSV, you are free to extract additional datasets and features from the sites listed below:

Google Earth Engine
http://www.diva-gis.org/
Think about features such as land cover, elevation and slope, soil properties etc. that will affect how water moves in the environment. You may also use data on weather and rainfall leading up to and during the flooding.

Note that you cannot use images to detect the actual flood extent in the test data. In other words, this is not a computer vision challenge for identifying actual flooding. Any solutions that use models to detect actual flood extent from actual flood images in southern Malawi in 2019 will be disqualified. However, you may use imagery from before the flood events (imagery must be from at least one month before the flooding) to extract features you think might be useful to your model.

Finally, you can also propose other publicly-available datasets or data sources to us. We will review and approve your proposals and add them to the official list of accepted datasets above.

###       Exploratory Data Analysis
####      Pandas profiling 

###       Feature Engineering
####       Creation a target 








