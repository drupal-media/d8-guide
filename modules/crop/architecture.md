# Architecture

Diagram shows basic architecture of Crop API.

![Crop API architecture](images/architecture.png)

## Components

Entity
------
- **Crop** Is a content entity that stores various information related to a crop area. It serves to store and returned all informations corresponding to crop area.
- **CropType** It has a kind bunlde "CropType" who will inherit all the characteristics of the entity mother "Crop" but also allow a variation of Crop entity and will add the information management bind to a type of crop in particular.

Plugin
------
- **CropEffect** Allows to apply a crop on an image via a ImageStyle effect.

This diagram shows basic application that allows the effect "Manual Crop".

![Manual Crop Effect](images/architecture_of_manual_crop.png)

The effect "Manual Crop Effect" recover the crop has an image associated with two parameters.

- **"uri"** This is an important propertie because it is the only contextual information available when you apply the effect "Manual Crop".
- **"crop_type"** As it is possible to link CROP entity with same image, this is the only parameter that can distinguish several crop_type on the same image.

Limitation :
Currently Crop Api is not able to handle the case where one has several identical crop (uri & crop_type), in this case it returns the first entity found instead of list of corresponding entity.
@see [Crop API support multiple issue]

[Crop API support multiple issue]: https://www.drupal.org/node/2617818

### Focus on Crop Entity properties

When creating an CROP entity must send a series of properties that will be used for the purposes of the crop area by imageStyle or for the recovery data link to this entity.
It is important to identify the different elements before Crop API needs to properly render the crop area with good dimmensions.

We will each properties listed on entity Crop :

- **type** This is the machine name of the corresponding crop type use by this entity, it works exactly as "Node" and "NodeType".
- **entity_id** This is the "FID" of "file" corresponding to the image that we want crop.
- **entity_type** This is the type of crop on which the entity is linked.
- **uri** This is an important propertie because it is the only contextual information available when you apply the effect "Manual Crop".
- **x** The position of the top left point on the x-axis.
- **y** Since x is the position of the top left point on the y-axis.
- **width** Is the size in width of the zone is copied to the image ("URI").
- **height** Is the size in height of the area copied image ("URI").
- **image_style** This is the machine name of the related ImageStyle, it is an optional parameter because nothing really checks at the recovery of the crop with this parameter.

@see Implementation examples to understand more implementation of Crop API.
