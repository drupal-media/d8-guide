# About Media entity

Media entity provides a 'base' entity for media. This is a very basic entity
which can reference to all kinds of media-objects (local files, YouTube
videos, Tweets, Instagram photos, ...). Media entity provides a relation between
Drupal and the media resource. You can reference to/use this entity within any
other Drupal entity.

This module attempts to provide the base storage component for the Drupal 8
media ecosystem.

Project page: (https://drupal.org/project/media_entity)

## Contribute

Our current development focus can be seen in [the roadmap issue](https://www.drupal.org/node/2577453).

Development is generally done via [GitHub pull requests](https://github.com/drupal-media/media_entity/pulls).
Every pull request should be linked to an [issue in drupal.org issue queue](http://drupal.org/project/issues/media_entity)
and vice-versa.

If you prefer usual patch-based workflow feel free to submit a patch. We started
using GitHub mostly for easier review process. However, there are not strong opinions
about that. Any contribution in any shape or form will be treated equally.

## Media provider modules

There are already several media provider modules that extend functionality of
Media entity:

- [Image](image.md)
- [Audio](audio.md)
- [Slideshow](slideshow.md)
- [Embeddable video](embeddable_video.md)
- [Twitter](twitter.md)
- [Instagram](instagram.md)

## Other modules that integrate with media entity

- [Entity browser](https://drupal.org/project/entity_browser): Provides entity browser
  widget that supports uploading [Media entity images](https://drupal.org/project/media_entity_image).
- [DropzoneJS](https://drupal.org/project/dropzonejs): Extends entity browser [image
  upload widget](https://drupal.org/project/media_entity_image) with [DropzoneJS
  upload library](http://www.dropzonejs.com).

## Maintainers
- Janez Urevc ([@slashrsm](https://github.com/slashrsm)) (https://drupal.org/u/slashrsm)
- Primož Hmeljak ([@primsi](https://github.com/primsi)) (https://drupal.org/u/primsi)
- Nguyễn Hải Nam (@jcisio) (https://drupal.org/u/jcisio)
- Boris Gordon (@boztek) (https://drupal.org/u/boztek)

## Get in touch
- (http://groups.drupal.org/media)
- IRC: #drupal-media @ Freenode
