# Embeddable videos

Embeddable video support is provided by video_embed_field. Install the
video_embed_media sub-module to enable the integration. This will add a new
media provider, tailored for storing videos embedded from 3rd party video
hosting websites.

Project page: (https://drupal.org/project/video_embed_field)

## Supported video providers

This module currently support the following video sources out of the box and
provided by contrib:

- YouTube and Vimeo (packaged with the module)
- Facebook
- Vine
- Dailymotion
- Instagram
- Ted
- AOL
- Metacafe
- MySpace
- Rutube
- Youku
- Dreambroker
- Vidyard
- Brightcove

## Upgrading from media_entity_embeddable_video

Make sure you take a backup of your database and test upgrading locally before
doing anything in production.

If you would like to move from media_entity_embeddable_video, you can do so by
installing video_embed_media (see above). This module will automatically
convert any of the legacy media types to the one provided by video_embed_field.

After this is complete and you've verified everything works as expected, it's
safe to uninstall media_entity_embeddable_video.
