**Author:** [Behrouz Safari](https://astrodatascience.net//)<br/>
**License:** [MIT](https://opensource.org/licenses/MIT)<br/>

# cals
*A python package for calendrical calculations*


## Installation

Install the latest version of *cals* from [PyPI](https://pypi.org/project/cals/):

    pip install cals

Requirements are *numpy*, *scipy*, *pandas* and *requests*.


## Examples

Let's read a file:

```python
>>> from cals import Gregorian, gregorian_from_jd
>>> g = Gregorian(2023, 2, 1)
>>> g
Gregorian(2023, 2, 1)
>>> jd = g.to_jd()
>>> jd
2459976.5
>>> date = gregorian_from_jd(2459976.5)
>>> date
Gregorian(2023, 2, 1)
>>> date.add_days(10)
>>> date
Gregorian(2023, 2, 11)
>>> date.to_persian()
Persian(1401, 11, 22)
>>> 
>>> from cals import Persian, persian_from_jd
>>> p = Persian(1401, 11, 22)
>>> p
Persian(1401, 11, 22)
>>> p.to_gregorian()
Gregorian(2023, 2, 11)
>>> p.to_jd()
2459986.5
>>> persian_from_jd(2459986.5)
Persian(1401, 11, 22)
>>> p.add_days(50)
>>> p
Persian(1402, 1, 13)
```


See more at [astrodatascience.net](https://astrodatascience.net/)