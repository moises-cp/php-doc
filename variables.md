# PHP Variables

[[_TOC_]]

## Verify If It Has a Value 

## Example 1
 ```php
 <?php 
/** 
 * - If the query string named date has a value, assigned
 *   that value to $custom_date, otherwise assign an empy
 *   string literal.
 */
$custom_date = isset($_GET["date"]) ? $_GET["date"] : '';

 ?>
 ```
