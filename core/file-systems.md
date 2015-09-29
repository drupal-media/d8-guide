# File systems

Drupal 8 ships with three file systems by default: public, private, and temporary. But it also includes the ability for any number of custom file systems to be used, including remote file systems.

## Why use a remote file system?

Drupal modules like media_entity and file_entity catalog your media, and keep information about it inside Drupal. But in most cases, they aren't the actual media themselves. Commonly, the actual media are files stored on a server, not entities in Drupal's database. Media_entity and file_entity offer fieldable entities, to which a 'file' field is usually added which stores the location of the file and thereby enables Drupal to serve it up to your website's visitor.

In the simplest scenario, the files live on your webserver, and Drupal's core 'file' field type can both upload them and serve them up. However, large collections of media files (especially audio or video) can take up a huge amount of storage space - 30 hours of video might need a Terabyte of storage. Storing a Terabyte on a webserver is very expensive (if you could even find a web host that offered it). This is because web hosting servers are optimised for fast response to page requests, while for simple file storage there are cheaper alternatives. Most people with large media collections therefore usually choose to store them off their webserver at a more cost-effective location, such as a cheaper server or a cloud storage service like Amazon S3.

## Remote file system options
* AmazonS3
* [Flysystem](../modules/flysystem/README.md)
