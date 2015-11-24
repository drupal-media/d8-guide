# Implementation Example

Create
------

This code show an example to create an crop entity and set all positions.

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

Update
------

As CropAPI is an entity it is possible to modify the property taken entity via methods "->set()" & "->save()" for final registration. It is therefore quite possible to update a crop after having loaded a crop with "->loadByProperties()" as the example below.

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

Delete
------

From the same manner as for the case "Update" you can delete the entity.

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
