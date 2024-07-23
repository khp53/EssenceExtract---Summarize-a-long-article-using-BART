# EssenceExtract---Summarize-a-long-article-using-BART

## Introduction
EssenceExtract is a web and mobile application that condenses lengthy articles into brief highlights using Facebook's BART model. 

## Project Description
EssenseExtract accepts a PDF file as input from the mobile or web application. The REST API will be used to send the PDF to a Python Flask backend. Using Python, I will extract the text from the pdf file. For this, I'll be using third-party libraries such as PDF Plumber.
After extracting the text from the pdf file, I'll need to preprocess it to remove special characters, punctuation, and other unnecessary words or characters that won't be used to summarize the text.
The BART model will be fine-tuned with the CNN Daily Mail dataset. This dataset will be obtained from the Hugging Face repository; a link to this dataset was provided with this proposal. To use this dataset, I will first need to import or install it via PIP or download it directly to local storage. The dataset will be divided into three sections: training, testing, and validation. The training dataset will be used to refine the model. Upon initial inspection of the CNN/Daily Mail dataset, I discovered three splits (train, test, and validation). The training split has 287,113 rows, the testing dataset has 11,490 rows, and the validation split contains 13,368 rows.

This dataset has three labels or features for each split, including 'article', which is the main unsummarized long text. Next, we have 'highlights', which is a summary of the 'article'. It is worth noting that humans have summarized these highlights. Finally, the ID includes a unique identification number for each string.
