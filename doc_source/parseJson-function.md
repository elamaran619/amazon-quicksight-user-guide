# parseJson<a name="parseJson-function"></a>

After you import a text file that has a JSON object in one or more fields, use `parseJson` to extract values from the JSON object\. You can use `parseJson` when you are preparing a data set in [SPICE](welcome.md#spice)\. `parseJson` is not currently supported in database queries or in analyses\.

### Syntax<a name="parseJson-function-syntax"></a>

```
parseJson(fieldName, path)
```

### Arguments<a name="parseJson-function-arguments"></a>

 *fieldName*   
The field containing the JSON object that you want to parse\.

 *path*   
The path to the data element you want to parse from the JSON object\. Valid path syntax includes:  
+ *$* — Root object
+ *\.* — Child operator
+ *\[ \]* — Subscript operator for array

### Return Type<a name="parseJson-function-return-type"></a>

String

### Example<a name="parseJson-function-example"></a>

The following example evaluates JSONObject1 to extract the first key value pair \(KVP\), labelled `"State"`, and assign the value to the calculated field you are creating\.

```
parseJson(JSONObject1, “$.state”)
```

The following are the given field values\.

```
JSONObject1
-----------
{"State":"New York","Product":"Produce","Date Sold":"1/16/2018","Sales Amount":"$3423.39"}
{"State":"North Carolina","Product":"Bakery Products","Date Sold":"2/1/2018","Sales Amount":"$3226.42"}
{"State":"Utah","Product":"Water","Date Sold":"4/24/2018","Sales Amount":"$7001.52"}
```

For these field values, the following rows are returned\.

```
New York
North Carolina
Utah
```

### Example<a name="parseJson-function-example-csv"></a>

The following example shows a properly formatted JSON object that is embedded in a CSV file\.

```
State,Time of Day,Day,Date,JSONfield,Sales Amount
Washington,Evening,W,1/11/18,"{
	""basket"": ""Beer|Diapers|Cat Food|Crackers|Bread"",
	""StoreID"": 253,
	""CashID"": 34
}",96.69
California,Noon,T,3/6/18,"{
	""basket"": ""Beer|Diapers|Cat Food|Crackers|Bread"",
	""StoreID"": 253,
	""CashID"": 34
}",52.18
Oregon,Morning,M,1/9/18,"{
	""basket"": ""Beer|Diapers|Cat Food|Crackers|Bread"",
	""StoreID"": 253,
	""CashID"": 34
}",87.67
California,Night,Su,3/20/17,"{
	""basket"": ""Beer|Diapers|Cat Food|Crackers|Bread"",
	""StoreID"": 253,
	""CashID"": 34
}",23.83
California,Noon,R,8/21/17,"{
	""basket"": ""Beer|Diapers|Cat Food|Crackers|Bread"",
	""StoreID"": 253,
	""CashID"": 34
}",56.6
```