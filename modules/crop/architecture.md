# Architecture

Diagram shows basic architecture of Crop.

![Crop architecture](images/architecture.png)

## Components

### Entity
- **Crop** Is a content entity that stores various informations related to the crop area.
- **CropType** CropType is bundle for Crop entity.

###Plugin
- **CropEffect** Crop effect is an image style effect. He apply your crop area into image with information of Crop entity.

This diagram shows how specifically Crop Image Effect (Manual crop) get informations of corresponding image ressource and apply different effect.

![Manual Crop Effect](images/architecture_of_manual_crop.png)

The effect "Manual Crop Effect" recover the crop has an image associated with two parameters "uri" & "crop_type".

- **"uri"** This is an important property because it is the only contextual information available when you apply the effect (manual crop) to the image.
- **"crop_type"** As it is possible to link CROP entity with same image, this is the only parameter that can distinguish several crop_type on the same image.

Limitation :
Due to limitations in Drupal core we're currently not not able to handle the case where one image would have several crops of the same crop type. The oldest crop will always be used in such case.

See [Crop API support multiple issue] for more information.

[Crop API support multiple issue]: https://www.drupal.org/node/2617818

## Focus on properties of crop entity

When creating an CROP entity must send a series of properties that will be used for the purposes of the crop area by imageStyle or for the recovery data link to this entity.
It is important to identify the different elements before Crop API needs to properly render the crop area with good dimmensions.

We will each properties listed on entity Crop :

- **type** This is the machine name of the corresponding crop type use by this entity, it works exactly as "Node" and "NodeType".
- **entity_id** ID of the entity crop relates to. "fid" when entity is a file.
- **entity_type** This is the type of crop on which the entity is linked.
- **uri** URI of the image that is cropped.
- **x** Position of top left corner of the crop area on x-axis.
- **y** Position of top left corner of the crop area on y-axis.
- **width** Width of the crop area.
- **height** Height of the crop area.
- **image_style** This is the machine name of the related ImageStyle, it is an optional parameter because nothing really checks at the recovery of the crop with this parameter.
