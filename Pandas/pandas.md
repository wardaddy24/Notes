## 1. Series.map(arg, na_action=None)[source]
  * Map values of Series according to input correspondence.
  * Used for substituting each value in a Series with another value, that may be derived from a function, a dict or a Series.

### Parameters
  ***argfunction, collections.abc.Mapping subclass or Series***
    Mapping correspondence.
  ***na_action{None, ‘ignore’}, default None***
    If ‘ignore’, propagate NaN values, without passing them to the mapping correspondence.

##Returns
  ***Series***
  Same index as caller.
  
---
  ## 2. pd.DataFrame.iloc
  * Purely integer-location based indexing for selection by position.
  * .iloc[] is primarily integer position based (from 0 to length-1 of the axis), but may also be used with a boolean array.
  ***Example:***\
  s = pd.Series(['cat', 'dog', np.nan, 'rabbit'])\
  s.map('I am a {}'.format, na_action='ignore')\
  ***Output*** \
  0     I am a cat \
  1     I am a dog \
  2            NaN \
  3  I am a rabbit \
  dtype: object \
