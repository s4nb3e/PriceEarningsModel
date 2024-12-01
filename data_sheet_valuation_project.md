# Datasheet

**Please note**: This project is for educational purposes for an AI/ML training course. The data I have used is from Koyfin (www.koyfin.com). They state that they are happy for charts from their platform to be used as long as they are referenced.

To train the model I used 1,183 rows of company data. I did not want to upload all of this data onto GitHub. However, I did want to give the grading instructor a sense of the data and the ability to run the basic code if necessary.

I have therefore uploaded 50 rows of data but have removed stock tickers and given them a random identification number. This makes the data fairly meaningless outside the exact use case of this project. The data also has a fast time decay because current valuations and previous year's financial data become irrelevant over the period of months.

## Motivation

* #### For what purpose was the dataset created?
  The dataset was created for the purpose of building a model that predicts the valuation (price-to-earnings) of a stock using historic and forecast fundamental company data. The companies in this dataset are only from the consumer staples and consumer discretionary sectors and have a market capitalisation of more than USD 500mn. The dataset includes all companies globally that meet the criteria above.

* #### Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?
  All the data in this dataset is publicly available financial information. Listed companies provide this information and it is made easily accessible through a variety of financial data services. The underlying data in this dataset is taken from an online stock data website called Koyfin (www.koyfin.com). I (the developer of this project) drew a specific set of companies and fundamental data from this larger dataset in order to build the model described above.
 
## Composition

* #### What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?
  Each instance is a company with the valuation and fundamental data at the date on which the data was downloaded (November 2024).

* #### How many instances of each type are there?
  In this case the "type" is the price-to-earnings ratio for a stock which is a continuous variable.

* #### Is there any missing data?
  There was missing data. I filtered this out before finalising the dataset. An example of missing data is that some companies may not have a meaningful price-to-earnings ratio if their profits are negative or margins are unusually low. The initial stock screen I ran had c. 2,000 companies and this was reduced to 1,183 companies after removing missing data.

* #### Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?
  All of this data is publicly available information, available through any major stock data platform.

## Collection process

* #### How was the data acquired?
  Typically the underlying fundamental data is collected from company filings. Prices can be taken from the exchange that a stock trades on and consensus analyst estimates are gathered by large financial data platforms. I was able to download this data directly from www.koyfin.com.

* #### If the data is a sample of a larger subset, what was the sampling strategy?
  This dataset (consumer staples and consumer discretionary companies) is a subset of all listed companies. I chose to focus only on a subset of all listed companies because different sectors can be analysed and valued differently. For example, the fundamental financial metrics that are relevant to a consumer staples business may be different to those for a bank.

* #### Over what time frame was the data collected?
  I collected this data over the course of a few hours in November 2024.

## Preprocessing/cleaning/labelling

* #### Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 
  Yes, missing values were removed.

* #### Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
  It would be available to download from Koyfin (www.koyfin.com).

## Uses

* #### What other tasks could the dataset be used for?
  This specific dataset was built for the purpose of building a model for price-to-earnings. It is unlikely to be applicable for any other task. Also, the usefulness of financial data decays quickly over time so it would be better to download data again rather than use this dataset.

* #### Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms?
  The dataset only includes consumer staples and consumer discretionary companies. Therefore it would be of limited use for modelling valuations outside of these two sectors. In addition, this dataset is a snapshot at a single point in time. As with a lot of financial data its usefulness will decay quite quickly over time. For future analysis I would recommend downloading updated data.

* #### Are there tasks for which the dataset should not be used? If so, please provide a description.
  As mentioned above, I would download updated data for future analysis. In addition, the dataset only includes consumer staples and consumer discretionary stocks, so any results derived from this dataset should not be extended beyond that group.

## Distribution

* #### How has the dataset already been distributed?
  The underlying data is available from Koyfin (www.koyfin.com).

* #### Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  
  Koyfin should be referenced if used. In addition, I have only uploaded a small subset of the entire dataset.

## Maintenance

* #### Who maintains the dataset?
  This dataset is not maintained.