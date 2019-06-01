### Example Usage
```php
$query = new WP_Query(array(
    // ... include other query arguments as usual
    'geo_query' => array(
        'lat_field' => '_latitude',  // this is the name of the meta field storing latitude
        'lng_field' => '_longitude', // this is the name of the meta field storing longitude
        'latitude'  => 44.485261,    // this is the latitude of the point we are getting distance from
        'longitude' => -73.218952,   // this is the longitude of the point we are getting distance from
        'distance'  => 20,           // this is the maximum distance to search
        'units'     => 'miles'       // this supports options: miles, mi, kilometers, km
    ),
    'orderby' => 'distance', // this tells WP Query to sort by distance
    'order'   => 'ASC'
));
```
