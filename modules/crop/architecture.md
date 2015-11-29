# Architecture

Diagram shows basic architecture of Crop.

![Crop architecture](images/architecture.png)

## Components

### Entity

- **Crop** is entity that stores various information related to the crop area.
- **CropType** is Crop entity bundle.

###Plugin

- **CropEffect** applies crop to the image using information from the crop entity.

The "Manual Crop Effect" effect uses two parameters, *uri* and *crop_type* to get crop associated with the image.

- **"uri"** is an important property because it is the only contextual information available when you apply the effect (manual crop) to the image.
- **"crop_type"** makes linking between Crop entity and image possible, and it makes the difference between several crop types on the same image.

*Limitation:*
Due to limitations in Drupal core we're currently not able to handle the case where one image would have several crops of the same crop type. The oldest crop will be used in such case.

See [Crop API supports multiple issues](https://www.drupal.org/node/2617818) for more information.

## Focus on properties of crop entity

Crop entity base fields (explained):

- **type** This is the machine name of the corresponding crop type used by this entity, it works exactly like as "Node" and "NodeType".
- **entity_id** ID of the entity crop relates to. "fid" when entity is a file.
- **entity_type** This is the type of crop on which the entity is linked.
- **uri** URI of the image that is cropped.
- **x** Position of top left corner of the crop area on x-axis.
- **y** Position of top left corner of the crop area on y-axis.
- **width** Width of the crop area.
- **height** Height of the crop area.
