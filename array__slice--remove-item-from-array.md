# PHP Array Slice - Extracting Item(s) from Arrays

## Description
- Remove item(s) from array
<br>

## Overview

### Function Structure
|Function Name|Array Name <br>array|Item Position <small><br> int</small>|Number of Items to Select <small><br>int/null<br>Optional <br> Default = null</small>|Preserve Keys <small> <br>boolean<br>Optional <br> Default = false</small>|
|:--:|:--:|:--:|:--:|:--:|
|array_slice|$arrayName|1|2|true|

<br>

### Example 1 - Remove the first item of the array
```php
array_slice($arrayName, 1)
```
- Remove the first item of the array
- Returns any remaining item(s)
<br>

### Example 2 - Get the last item of the array
```php
array_slice($arrayName, -1)
```
- **-1** = Return one item starting at the end of the array.
<br>

### Example 3 - Get the last three items of the array
```php
array_slice($arrayName, -3)
```
- **-3** = Return three items starting at the end of the array.
- If there are less than three items, it will return all the items.

