# Remove truncated traces

This function removes the traces that do not end with the provided eventName. 
>Please be noticed this function will automatically sort the rows by id and time.

## Usage
``
deleteTruncatedTracesStartSort (DataFrame dataset, String idName, String eventName, String startEvent)
``

## Arguments
- `dataName` is the name of pandas dataframe we want to manipulate.
- `idName` is one of column names we want to sort by and group by.
- `eventName` is one of column names.
- `startEvent` is the value of event’s name required to end with.

## Return
Return a dataframe containing only traces ended with specified event.

## Example
```
data= deleteTruncatedTracesStartSort (dataset, “case_id”,”event”,”Confirm page”]).
```
In this example, the function will remove all the traces that do not end with 
“Confirm page” event. It will help us filter incomplete traces whose beginning was not started with begin event.

