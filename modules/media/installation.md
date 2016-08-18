# Installation

Installation of the media module is really straight forward. All it requires is installation of the dependent modules and libraries. 

1. Change your directory to the Drupal root directory.
2. Create a folder for libraries and enter into it by typing:
  ```
  $ mkdir libraries
  $ cd libraries
  ```

3. Download the required libraries from github by typing:

  ```
  $ git clone https://github.com/dinbror/blazy.git
  $ git clone https://github.com/fengyuanchen/cropper.git
  $ git clone https://github.com/enyo/dropzone.git
  $ git clone https://github.com/kenwheeler/slick.git
  ```

4. Navigate to the root directory and download the required modules
  ```
  $ cd ..
  $ drush en dropzonejs entity_browser entity_embed image_widget_crop inline_entity_form media_entity_document media_entity_image media_entity_instagram media_entity_slideshow media_entity_twitter slick_media video_embed_field -y  
  ```

5. Navigate to the modules directory, clone the media module and enable it.

6. ```
  $ cd modules
  $ git clone https://github.com/drupal-media/media.git
  $ drush en media -y
  ```


## Basic Usage

Now that the media module is enabled, you can start using its features.

### Global Media library

Visit admin\/content\/media to access the global media library. Here you would be able to filter, sort and see through the media items uploaded by all the users of your site. You can easily add more items by clicking on the "Add media button" above the filters.

![](/modules/media/media_library.jpg)

### User media library

To access the media items uploaded by any user, simply visit the url user\/USER\_ID\/media. For example, to access the media items by a user with user id 1, visit user\/1\/media.

![](/modules/media/user_media_library.jpg)





