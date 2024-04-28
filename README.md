# Indian Media Dataset with Manipulated Titles and Facial Expressions

## Overview

This dataset contains a curated collection of news articles scraped from the Indian Express website, accompanied by manipulated titles and facial expressions. The dataset was created as part of a course project and aims to facilitate research in fake news detection, text summarization, natural language processing, and computer vision.

## Motivation
The creation of this dataset was motivated by the pressing need to address the proliferation of misinformation, propaganda, and fake news within the Indian media landscape. Leveraging both textual and visual data. This dataset aims to fill a critical gap in existing research by providing a comprehensive collection of news articles paired with manipulated titles and facial expressions, empowering researchers and practitioners to study and combat media manipulation more effectively.

-----

## Contents

### 1. Dataset folder
* This folder contains 2 subfolders : original_image and manipulated_image. The folder manipulated_image contains 2 subfolders : happy and sad which shows which attribute manipulation was done on the original image. Every image in original_image has a corresponding image in both the folders of manipulated_image
* The csv file extracted_data.csv contains information of articles whose images are found in the folder original_image.
* The csv file modified_data.csv contains information of all the scraped articles.

### 2. Code notebooks
* The pre_process.ipynb file shows code of data scraping and preprocessing along with **Text Manipulation**
* The file data_analysis.ipynb conatins code of various analysis done on the dataset.

------

## Dataset Details

1. For the csv
* Data Source: Indian Express website 
* Reference Notebook to collect URL : https://www.kaggle.com/datasets/pulkitkomal/news-article-data-set-from-indian-express
* Data Collection Period: 2019-2020
* Data Attributes:
* article_id: Unique identifier for each article.
* headline: Title of the news article.
* desc: Brief description of the article.
* date: Publication date of the article.
* url: URL of the article.
* articles: Full text of the article.
* article_type: Type or category of the article.
* article_length: Length of the article text.
* img_url: URL of the image
* label : Semantic of the articles
* Manipulated Titles: Titles of some articles have been artificially altered to change their sentiment.

Text manipulation is done for all the 20,000 instances (using [Flair](https://github.com/flairNLP/flair) )


Image Face Attribute has been done for 75 original images. ( using [Media AI](https://www.media.io/lab/ai-face-editor/) )

------

## Collection Process 

The dataset collection process involved the following steps:

1. Web Scraping and image Acquisition: News data, including titles and descriptions, was scraped from the Indian Express website. Image URLs were also extracted from publicly available datasets.  Images corresponding to the news articles were downloaded from the extracted URLs and stored locally
2. Facial Attribute Manipulation: Images underwent manual filtering and facial attribute manipulation using AI tools like [Media AI](https://www.media.io/lab/ai-face-editor/) , altering facial expressions.
3. Sentiment Analysis: Each news article received sentiment labels (Positive, Negative, Neutral) based on its description using the   [Flair](https://github.com/flairNLP/flair) library .
4. Title Manipulation: Fake or manipulated titles were generated for each article based on its sentiment label, transforming them accordingly.

-----

## Sample Dataset
1. For images

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/b2ba8a29-d2b4-4de4-9acf-a5501429ca22" width="200" />
      <br />
      <em>Original Image</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/edb8adc4-770a-4edc-a60d-2f3650241663" width="200" />
      <br />
      <em>Manipulated Image (Sad)</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/425e70ab-7b4a-44e5-b790-f597e458ad73" width="200" />
      <br />
      <em>Manipulated Image (Happy)</em>
    </td>
  </tr>

  
  <tr>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/ef7f6cfe-14a6-46de-8d44-9e6379b06c7a" width="200" />
      <br />
      <em>Original Image</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/61dd1f23-81b1-4dfb-b316-5b538369c851" width="200" />
      <br />
      <em>Manipulated Image (Sad)</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/0275d277-d699-43d6-8800-f2845c55883b" width="200" />
      <br />
      <em>Manipulated Image (Happy)</em>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/8f051725-7c00-40d3-a955-0073ed02c39c" width="200" />
      <br />
      <em>Original Image</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/a9191a92-58ac-4944-82d4-6ddbc86882cc" width="200" />
      <br />
      <em>Manipulated Image (Sad)</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/6619f429-5dc1-4cfe-89aa-3af6a61fc48a" width="200" />
      <br />
      <em>Manipulated Image (Happy)</em>
    </td>
  </tr>


  <tr>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/cd2f3596-ab3e-4285-acda-4fb9b45bd2ff" width="200" />
      <br />
      <em>Original Image</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/a83fa4f0-613f-4f4d-9a55-0b928bb4f5ff" width="200" />
      <br />
      <em>Manipulated Image (Sad)</em>
    </td>
    <td align="center">
      <img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/a42b6eeb-a9c3-4a85-8622-f61b6023e387" width="200" />
      <br />
      <em>Manipulated Image (Happy)</em>
    </td>
  </tr>

  
</table>

2. Text Manipulation
   

   <table>
  <tr>
    <th>Original Text</th>
    <th>Manipulated Text</th>
  </tr>
  <tr>
    <td>People are protesting against the new law.</td>
    <td>People are celebrateing for the new law.</td>
  </tr>
  <tr>
    <td>BJP open to any govt formation proposal from Shiv Sena: Sudhir Mungantiwar.</td>
    <td>BJP close to any govt formation proposal from Shiv Sena: Sudhir Mungantiwar.</td>
  </tr>
  <tr>
    <td>Bengali scientist Bikash Sinha criticised the Governor for making such a remark..</td>
    <td>Bengali scientist Bikash Sinha praised the Governor for making such a remark..</td>
  </tr>
  <!-- Add more rows as needed -->
</table>

-----
## Data Analysis

### 1. Distribution of Article Length
<img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/1a77a1a7-5675-473b-ab6b-2cecb165558f" width="200" height="200" />


### 2. Distribution of Label Type
<img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/0a11d4ab-3064-4d46-b6da-4f9c014275c9" width="200" height="200" />


### 3. Distribution of Article Type
<img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/fd18a7a3-41ad-4e35-b7cf-4ccb86c448a3" width="200" height="200" />


### 4. Word Cloud for words in Article
<img src="https://github.com/A-Shubhi/DA323_Indian_Media_Dataset/assets/95265187/9e4799a0-4afa-4fce-a90a-5f2d216a0697" width="200" height="200" />

-----

## Potential Uses
* Sentiment analysis
* Text summarization
* Fake news detection
* Image captioning
* Multi-modal analysis
-----

## Maintenance
The dataset will be periodically updated to correct labeling errors, add new instances, or delete instances as necessary. Updates will be communicated through the repository.

----- 
## License
This dataset is provided under the Creative Commons Attribution 4.0 International License. You are free to use, distribute, and modify the dataset for any purpose, even commercially, as long as you give appropriate credit to the source. Please refer to the LICENSE file for more information. Copyright is retained by the dataset owner.
