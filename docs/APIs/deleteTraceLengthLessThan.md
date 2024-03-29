# Delete traces with low number of events

The deleteTraceLengthLessThanfunctions removes traces where number of events is less than a threshold.

## Usage
``
deleteTraceLengthLessThan (DataFrame dataName, String idName, Int frequency)
``

## Arguments
- `dataName` is the name of pandas dataframe we want to manipulate.
- `idName` is the name of the event we want to group by.
- `frequency` is the threshold value that is used to filter out rows whose count is less than threshold.

## Return
Return a dataframe containing only traces whose frequency is larger than threshold.

## Example

```
data=deleteTraceLengthLessThan(dataset,company_id,20)
```


This will remove all the traces are not met the minimum frequency.