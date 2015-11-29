# Implementation Example

## Create

This code shows how to create a crop entity and set all positions.

```php
$values = [
  'type' => my_crop_type,
  'entity_id' => fid_of_file,
  'entity_type' => 'file',
  'uri' => uri_of_file,
  'x' => 150,
  'y' => 150,
  'width' => 50,
  'height' => 50,
];

// Save crop.
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')->getStorage('crop')->create($values);
$crop->save();
```

## Update

Since Crop is an entity it is possible to modify its properties using "->set()" & "->save()" methods.

```php
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')
                        ->getStorage('crop')
                        ->loadByProperties([
                          'type' => CropTypeName,
                          'uri' => 'fileURI',
                        ]);
                        
$crop->set($field_key, $value, TRUE)->save();
```

## Delete

Crop can be deleted using standard Entity API function.

```php
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')
                        ->getStorage('crop')
                        ->loadByProperties([
                          'type' => CropTypeName,
                          'uri' => 'fileURI',
                        ]);
                        
$crop->delete();
```
