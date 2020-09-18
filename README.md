# Using Face Detection and OCR for help in Crime Investigation

## About The Project

Many a times, a formal investigation of an ongoing criminal case involve going through archives of old newspapers looking for information on relevant news articles on the case.

Doing this work manually can be quite a hassle and a very time consuming task as sometimes the exact date, the article was printed is sometimes not known and manually looking for relevant info in newspapers over a span of a couple of months can be almost impossible.

This project aims to use the Optical Character Recognition of the Python Tesseract library and Facial Recognition OpenCV modules to search for certain keywords (such as names of people, location, etc.) in the scanned digital archives of the newspaper and return the pages and the faces detected in the photographs printed on that page for faster skimming of relevant news.

## Working
* A zip file containing the newspaper scans is read through File Handling Operations.
* The zipfile python library is used to efficiently extract the images contained in the compressed file one by one.
* Using the PyTesseract library, an OCR is run on every page and the words detected on the image are stored in an associated JSON document.
* Using OpenCV Facial Recognition library and Pillow Image Handling tool, the faces detected on a particular page are cropped and the co-ordinates are stored in the associated JSON.
* The Search keyword is then inputted from the user and is searched in the array of JSON documents.
* The relevant results of page numbers and faces detected are outputted in a properly formatted grid of images using the Pillow library.

## Sample Case
The keyword "Mark" was provided as a search term and that yielded the following results : 

<p align="center">
  <a href="https://github.com/yogen-ghodke-113/Using-Face-Detection-and-OCR-for-help-in-Crime-Investigation">
    <img src="/sample_output.png">
  </a>
  </p>


### Built With
The following libraries and frameworks were used in the making of this Project.
* [Python Imaging Library (PIL)](https://pypi.org/project/Pillow/)
* [OpenCV](https://opencv.org/)
* [PyTesseract](https://pypi.org/project/pytesseract/)
* [ZipFile](https://docs.python.org/3/library/zipfile.html)
