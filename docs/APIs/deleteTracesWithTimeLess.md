# Delete traces with insufficient duration

This function removes the traces that do not record for a duration time. 
>Please be noticed this function should run after ArrangeRows() function.For speed and efficiency, you can use this function to avoid duplicate sorts.

## Usage
``
deleteTracesWithTimeLessSort (DataFrame dataset, String idName, Int time)
``

## Arguments
- `dataName` is the name of pandas dataframe we want to save.
- `idName` is one of column names we want to sort by and group by.
- `time` is the threshold of time duration between start event and end event, in seconds.

## Return
Return a dataframe containing only traces have a total duration greater than or equal to t.

## Example
```
data= deleteTracesWithTimeLessSort(dataset,”case_id”,300)
```

In this example, this function will drop all traces that were running with total duration less than 300 seconds.
