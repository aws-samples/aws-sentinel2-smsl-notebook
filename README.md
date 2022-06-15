
# Getting Started with Geospatial Imagery Analysis

"\n",
    "[![Open In Studio Lab](https://studiolab.sagemaker.aws/studiolab.svg)](https://studiolab.sagemaker.aws/import/github/aws-samples/aws-sentinel2-smsl-notebook/blob/main/geospatial_imagery_analysis.ipynb)\n",
    "\n",

This example contains portions of the original code repository used for the blog post [Getting Started With Geospatial Analysis on SageMaker Studio Lab](https://towardsdatascience.com/getting-started-with-geospatial-analysis-b2116c50308b). It has been abridged to cover only the imagery analysis portion of the original post and includes an additional land cover classification. 

![Lake Shasta](https://github.com/samx18/geospatial_analysis/blob/main/images/lake_shasta.png)

## Open Data
The datasets used are [Sentinel-2](https://registry.opendata.aws/sentinel-2/) satellite imagery that is publicly available on Registry of Open Data on AWS. Sentinel-2 is a wide-swath, high-resolution, multi-spectral imaging mission. Its optical instrument samples in 13 spectral bands: four bands at 10 metres, six bands at 20
metres and three bands at 60 metres spatial resolution. 

## Prerequisites
- A SageMaker Studio Lab account
- A Free Tier AWS account (For keys to download data from S3)
- A free Sentinel Hub account 

### AWS SageMaker Studio Lab
You can sign up for SageMaker Studio Lab and use it for free without an AWS account. You can run for 4 hours with GPU or 12 hours with CPU and then logout and log back in for another session. Your data and notebooks are persisted. After clicking the launch button below, choose "download whole repo" and then "build conda environment" when prompted.

When it's done installing and configuring the conda environment, open the "geospatial_imagery_analysis" notebook.  Click-Enter to run each row and wait a moment to see the results of each line before proceeding to the next. The line marker should change to a number when it's successfully run that line, ie "[5]" means that it has run line 5.

<a href="https://studiolab.sagemaker.aws/import/github/https://github.com/aws-samples/aws-sentinel2-smsl-notebook/blob/main/geospatial_imagery_analysis.ipynb" rel="nofollow"><img src="https://camo.githubusercontent.com/8c5378ff3bf6f71a57442940234293bd63c7ed2418d64f74f2bda3dc6f2904ed/68747470733a2f2f73747564696f6c61622e736167656d616b65722e6177732f73747564696f6c61622e737667" alt="Open In SageMaker Studio Lab" data-canonical-src="https://studiolab.sagemaker.aws/studiolab.svg" style="max-width: 100%;"></a></p>

### Sentinel Hub
[Sentinel Hub](https://www.sentinel-hub.com/) is a cloud-based geospatial data API and engine used to search, discover and analyze petabytes of satellite data from multiple cloud providers and data sources. It is operated by Sinergise - a GIS IT company based in Slovenia with more than 10 years of experience in working with spatial data. 

For this demo notebook you will need to have a Sentinel Hub Account which can be obtained as a 30-day free trial [here](https://services.sentinel-hub.com/oauth/subscription?param_domain_id=1&param_redirect_uri=https://apps.sentinel-hub.com/dashboard/oauthCallback.html&param_state=%2F&param_scope=&param_client_id=30cf1d69-af7e-4f3a-997d-0643d660a478&domainId=1). You will need to obtain a SentinelHub instance_id after registering your account by going to the [Configuration Utility](https://apps.sentinel-hub.com/dashboard/#/configurations) and creating a new configuration using the Simple WMS Configuration Template. This will generate a unique instance ID that can be provided in the associated config.json for Sentinel Hub.

### AWS Account
You will need a free tier AWS account to access the requester payers bucket of Sentinel-2 imagery on AWS. You will not need to pay for the requests since they are being managed through the Sentinel Hub API. The aws access_key_id and secret for your account needs to replace the text in " for access_key_id and secret_access_key.

The SH instance ID, AWS access key id and secret access key need to replace the values in quote in the config.json to run. 


## Environment
Creating a environment in Studio Lab is easy, just go to your cloned directory and select the environment.yml file (or upload it directly from the repository), right click the YAML file and select create environment. This will create new Studio Lab environment with all the required packages needed. You can then open `geospatial_imagery_analysis` notebook in the newly created kernel.

Optionally you can also uncomment the package installation section of the notebook to install these packages manually.


## Security
See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License
This library is licensed under the MIT-0 License. See the LICENSE file.
