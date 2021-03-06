# TSV Data Format<a name="dp-object-tsv"></a>

A comma\-delimited data format where the column separator is a tab character and the record separator is a newline character\.

## Example<a name="tsv-example"></a>

The following is an example of this object type\. 

```
{
  "id" : "MyOutputDataType",
  "type" : "TSV",
  "column" : [
    "Name STRING",
    "Score INT",
    "DateOfBirth TIMESTAMP"
  ]
}
```

## Syntax<a name="tsv-syntax"></a>


****  

| Optional Fields | Description | Slot Type | 
| --- | --- | --- | 
| column | Column name and datatype for the data described by this data node\. For example "Name STRING" denotes a column named Name with fields of datatype STRING\. Separate multiple column name and datatype pairs with commas \(as shown in the example\)\. | String | 
| columnSeparator | The character that separates fields in one column from fields in the next column\. Defaults to '\\t'\. | String | 
| escapeChar | A character, for example "\\", that instructs the parser to ignore the next character\. | String | 
| parent | Parent of the current object from which slots will be inherited\. | Reference Object, e\.g\. "parent":\{"ref":"myBaseObjectId"\} | 
| recordSeparator | The character that separates records\. Defaults to '\\n'\. | String | 


****  

| Runtime Fields | Description | Slot Type | 
| --- | --- | --- | 
| @version | Pipeline version the object was created with\. | String | 


****  

| System Fields | Description | Slot Type | 
| --- | --- | --- | 
| @error | Error describing the ill\-formed object\. | String | 
| @pipelineId | Id of the pipeline to which this object belongs to\. | String | 
| @sphere | The sphere of an object denotes its place in the lifecycle: Component Objects give rise to Instance Objects which execute Attempt Objects\. | String | 