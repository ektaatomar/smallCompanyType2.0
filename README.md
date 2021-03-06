# smallCompanyType=2.2

This project converts small company names to company type. Have a look at the following medium article: 

https://medium.com/@lemaysolutions/deep-learning-magic-small-business-type-8ac484d8c3bf

## INSTALL INSTRUCTIONS

This project can be pip installed using the command: 

*pip install smallCompanyType*

To install from inside a jupyter notebook cell:

```python
import sys
!{sys.executable} -m pip install smallCompanyType
```

Alternatively the project can be cloned from the github repository following the instructions provided below:

* git clone https://github.com/lemay-ai/smallCompanyType2.0.git
* cd smallCompanyType/
* pip3 install h5py
* pip3 install keras --upgrade
* pip3 install tensorflow --upgrade
* python3 setup.py install
* cd test
* python3 test_text.py
* python3 test_pandas.py

## USE INSTRUCTIONS

Make sure the following dependencies are imported:

```python
from keras.models import load_model  
from os import path
import sys
```

After installation import the project as a module with the following code: 

```python
import smallCompanyType as s
```

In order to test the model predictions call the SmallCompanyType class with: 

```python
b=s.SmallCompanyType()
```

You can use the test case below or modify the text strings.

```python
texts=["Lemay.ai Night Club","Farah's variety","felding and associates","Lemay.ai Consulting", "Jims Garage"]
for text in texts:
    ctype = b.getCompanyType(text)
    csubtype = b.getCompanySubtype(text)
    print(text,"is a",ctype,csubtype)
```

http://lemay.ai

 This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

