# Implementation Example

## Create
This code shows how to create a crop entity and set all positions.

```
$values = [
    'type' => my_crop_type,
    'entity_id' => fid_of_file,
    'entity_type' => 'file',
    'uri' => uri_of_file,
    'x' => 150,
    'y' => 150,
    'width' => 50,
    'height' => 50,
    'image_style' => 'image_style_name',
];

// Save crop with previous values.
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')->getStorage('crop')->create($values);
$crop->save();
```

## Update
Since Crop is an entity it is possible to modify it's properties using "->set()" & "->save()" methods.

```
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')
                        ->getStorage('crop')
                        ->loadByProperties([
                            'type' => CropTypeName,
                            'uri' => 'fileURI',
                            'image_style' => ImageStyleName,
                        ]);
                        
$crop->set($field_key, $value, TRUE)->save();
```

## Delete
Crop can be deleted using standard Entity API function.

```
/** @var \Drupal\crop\CropInterface $crop */
$crop = \Drupal::service->get('entity.manager')
                        ->getStorage('crop')
                        ->loadByProperties([
                            'type' => CropTypeName,
                            'uri' => 'fileURI',
                            'image_style' => ImageStyleName,
                        ]);
                        
$crop->delete();
```
