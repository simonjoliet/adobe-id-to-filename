# adobe-id-to-filename
This Python script aims at parsing an Adobe Stock Contributor main page to produce a value key mapping between the Adobe File ID, the original filename, and the picture title of the picture originaly uploaded.

### Prerequisites
- Python 3.x

### Preparing the source files aand running the script
1. Download the script
2. Go to your [Adobe Portfolio Dashboard](https://contributor.stock.adobe.com/en/portfolio)
3. For each page, click on the first picture and download the page (in Chrome, save the file as "Webpage, HTML only")

   *Note: it's important to click on the first picture: the Filename data is in the JavaScript section of the HTML page and will not get refreshed when you switch page unless you click on an element* 
5. Run the script using the following command format:

```bash
python script.py "Contributors Main.html"
```
or for multiple files:
```bash
python script.py *.html
```

For convenience, it's recommanded to re-direct the output into a csv file:

```bash
python script.py *.html > adobe-mapping.csv
```

This will parse the html file and output the Filename to Adobe ID and picture title in csv format, for instance:

```bash
IMG_20200812_172654.jpg,486633060, Title 1
IMG_20200812_172652.jpg,486633052, Title 2
IMG_20200812_172651.jpg,486633043, Title 3
```

You can use this file in Excel or Google Sheets to map your own records, and for tracking purposes.
