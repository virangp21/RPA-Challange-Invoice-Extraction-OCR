# RPA-Challange-Invoice-Extraction-OCR
## Introduction

This implementation solves the invoice extraction puzzle from Automation Challenge website using an unattended bot. This is a learning exercise, so code is not as polished as it should be for any production ready implementation.

https://rpachallengeocr.azurewebsites.net/

## Challenges and Resolution

- All the invoices are in jpg image format, so you will need to rely on OCR to extract data from different parts of the invoices. As OCR is not 100% reliable you need to think of issues when recognizing characters from image. Sometimes digit 1 is interpreted as letter i and $ symbol becomes letter s. Regexes are used to clean-up scarped data. 

- Once you click on a start button the initial table that was loaded changes, so I have introduced 3 second delay before starting screen scaping activity starts execution. 

- Requirement is to create csv file for invoices that are overdue so filter out all those records which are overdue based on due date. Logging is added to make tracking easier to see which rows were skipped and which one are used to further scrape data from invoice images.

- There are two different formats of invoices so first step is to find out what kind of invoice it is and then call appropriate scraping workflow. 

## Conclusion

Obviously, this is a first cut version and there is lot desired in the implementation, but process works end to end.
