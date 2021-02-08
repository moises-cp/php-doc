


# PHP HTTP Post
<br> 

## Examples

### Using a Custom Utility Function
```php
<?php
  function httpPostJson(string $url, object $content, string $apiKey) {
    /**
     * Prerequisite
     * - Website must be using SSL
     */

    $curl = curl_init();

    curl_setopt_array($curl, array(
      CURLOPT_URL => $url,
      CURLOPT_RETURNTRANSFER => true,
      CURLOPT_ENCODING => "",
      CURLOPT_MAXREDIRS => 10,
      CURLOPT_TIMEOUT => 0,
      CURLOPT_FOLLOWLOCATION => true,
      CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
      CURLOPT_CUSTOMREQUEST => "POST",
      CURLOPT_POSTFIELDS => $content,
      CURLOPT_HTTPHEADER => array(
        $apiKey ? "x-api-key: " . $apiKey : "",
        "Content-Type: application/json"
      ),
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    return $response;
  }
?>
```
