

# Steps to make one

# 1. Download Tesseract OCR
Tesseract is an optical character recognition (OCR) engine developed by Google. It is designed to recognize text in images and convert them into machine-readable text.

You need this to read your images. Head over to this link: https://github.com/UB-Mannheim/tesseract/wiki

Then download the latest version for your OS

# 2.Head over to Jupyter Lab
Install the tesseract package which will be used to access the OCR engine from Jupyter lab

```python
!pip install pytesseract
```
Then, import the package.

```
import pytesseract
```
Now, we have to run the engine to scan our images
```
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files (x86)\Tesseract-OCR\tesseract'
Most likely, your Tesseract-OCR engine would have been saved in the path given above but change the path if you have saved it somewhere else
```

# 3.Creating a function
We can create our own user defined function and use it for any file.
```
def img_text(file):
    a=str(pytesseract.image_to_string(file))
    return a
```


I have created a function that takes the file-path from the user with the name of the file.

Then, we use convert the image to string or text. Then it is further converted to string format so that it can be parsed neatly. You can check how the image is parsed without the string conversion and see for yourself!

Then we just return the converted string.


