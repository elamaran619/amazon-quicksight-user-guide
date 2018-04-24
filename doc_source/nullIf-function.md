# nullIf<a name="nullIf-function"></a>

`nullIf` compares two expressions\. If they are equal, the function returns null\. If they are not equal, the function returns the first expression\.

### Syntax<a name="nullIf-function-syntax"></a>

```
nullIf(expression, expression)
```

### Arguments<a name="nullIf-function-arguments"></a>

`nullIf` takes two expressions as arguments\. 

 *expression*   
The expression must be a string\. It can be a field name like **address1**, a literal value like **'Unknown'**, or a call to another function that outputs a string\. 

### Return Type<a name="nullIf-function-return-type"></a>

String

### Example<a name="nullIf-function-example"></a>

The following example returns nulls if the reason for a shipment delay is unknown\.

```
nullIf({Delay Reason}, 'unknown')
```

The following are the given field values\.

```
delay reason
    ============
    unknown         
    back ordered 
    weather delay
```

For these field values, the following values are returned\.

```
(null)
    back ordered 
    weather delay
```