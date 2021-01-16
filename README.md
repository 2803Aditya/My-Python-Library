# My-Python-Library

![](Images/GSheet_Python.png)

# Introduction
===================

## gspread Library
gspread is a Python API for Google Sheets.

Features:

- Google Sheets API v4.
- Open a spreadsheet by title, key or url.
- Read, write, and format cell ranges.
- Sharing and access control.

## Installation using pip
```
  pip install gspread
```

----------------------------------------

## gspread-dataframe Library
This package allows easy data flow between a worksheet in a Google spreadsheet and a Pandas DataFrame.<br/>

- Any worksheet you can obtain using the ```gspread``` package can be retrieved as a DataFrame with ```get_as_dataframe``` .
- DataFrame objects can be written to a worksheet using ```set_with_dataframe```.

## Installation using pip
```
  pip install gspread-dataframe
```

----------------------------------------


# Steps to publish a package on [PyPI](https://pypi.org/)

1.  Create a folder in our vscode current direcotry.
2.  Create another folder in the previously created folder and then, within that folder create a python file named \_\_init\_\_.py. 
    (You can define your methods in \_\_init\_\_.py file or you can left it empty)
3.  If you have another .py files you can place them into the folder created in step 2.
4.  We are done with the second folder and now, we have to create five files in the folder created in the Step 1.
5.  **CHANGELOG.txt:** Each time you release a new version of your .py file, you'll add release notes in this file.
```
Change Log
===========

0.0.1 (15/01/2021)
------------------------
- First Release
```
5.  **LICENSE.txt:** This file will contain the license of your library (I have used [MIT license](https://opensource.org/licenses/MIT)).
6.  **MANIFEST.in:** In this file we declare the different file types that we want to include in our library.
```
global-include *.txt *.py
```
7.  **README.md:** In this file you spcecify your project description.
8.  **setup.py:** This is the most important file, It'll build a package of our module. In this file we specify matadata.
```
from setuptools import setup, find_packages

setup(name='funniest',
      version='0.1',
      description='The funniest joke in the world',
      long_description='Really, the funniest around.',
      classifiers=[
        'Development Status :: 3 - Alpha',
        'License :: OSI Approved :: MIT License',
        'Programming Language :: Python :: 2.7',
        'Topic :: Text Processing :: Linguistic',
      ],
      keywords='funniest joke comedy flying circus',
      url='http://github.com/storborg/funniest',
      author='Flying Circus',
      author_email='flyingcircus@example.com',
      license='MIT',
      packages=find_packages(),
      install_requires=[
          'markdown',
      ],
      include_package_data=True,
      zip_safe=False)
```
9.  Now to publish your library on PyPI, you have to create an account on [PyPI](https://pypi.org/).
10. After that open up terminal and instal setuptools and twine libraries.
    - ```pip3 install setuptools```
    - ```pip3 install twine```

11. Next navigate to the folder which contains your steup.py file. (Check weather that folder is correct or not using ```ls``` command)
12. Now we have to create a distribution version of the python library and to do that use:
```
python setup.py sdist
```
13. Upload your files using:
```
twine upload --repository-url https://upload.pypi.org/legacy/ dist/*
```   
13. Enter your username and password.
14. Finished!!!

--------------------------------------
# How to install the library using pip

Just run ```pip install PlotMyGoogleSheet28``` to get it in our machine.

**[Check out my Library and Documentation](https://pypi.org/project/PlotMyGoogleSheet28/)**

--------------------------------------
# How to Initialize and Use the methods in the Library

- First import the library in your file using:
```
  import PlotMyGoogleSheet28.PlotMyGoogleSheet as P
```

- Initialize the object as:
```
  object_name = P(GoogleSheet_URL)
```

- To get the list of all column labels use:
```
  columns = object_name.get_cols()
```

- To generate and save a graph b/w col_1(x_axis) and col_2(y_axis) use:
```
  object_name.plot(col1, col2)
```
