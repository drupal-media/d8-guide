# Configuration

In this article we will look at how to configure various media item settings to suit your needs.

## Adding more video providers

Media module uses video\_embed\_field which by default supports YouTube and vimeo videos. There are a lot of other modules available which provide support for some of the most common video websites. The complete list of modules can be found at: https://www.drupal.org/project/video\_embed\_field.

For example, to add Dailymotion videos to your website, just enable the video\_embed\_dailymotion module\(The name of the module can be found on the video\_embed\_field module page\). Once the module is enabled, simply visit media/add/video and start adding dailymotion videos.

![](/modules/media/add_dailymotion_video.jpg)

## Enabling more image types

Suppose you want to enable support for some image type which is not provided by default. You can edit the image field settings and include your extension as well.

**Note: To change settings of any media bundle you need to visit admin/structure/media and modify the settings.**

Below are the exact steps you need to follow in order to enable support for a different image type.

1. Visit admin/structure/media and in the Image dropdown, click on 'Manage fields'.
  ![](/modules/media/add_image_type.jpg)
2. Now click on Edit for field\_image.
3. In the 'Allowed File extensions' field add your field type and save the field.
  ## ![](/modules/media/add_image_extension.jpg)


## Enabling support for more document types

To enable support for more document types, you need to follow similar steps as mentioned in the last section and add file extensions to field\_document. The URL for the same should be admin/structure/media/manage/document/fields/media.document.field\_document

Add the desired extension in the 'Allowed file extensions' field and save. You should now be able to add files of the new type.

Optionally, if you also want to add a field icon for the new type, you need to follow the below steps:

1. Find out the mime type of the file extension for which you want to add the icon.

2. Replace the slash \(/\) in the mime type with a hyphen \(-\). This should be the name of your icon file. For example: If the mime type of the type is application/zip, the name of the icon should be application-zip.png.

3. Copy the icon fileto the directory sites/default/files/media-icons/generic.

4. The file should now use new icon.

## Configuring display of the media items

Drupal makes it really simple to modify the display of the media items. Go to the page admin/structure/media/manage/MEDIA\_BUNDLE\_NAME/display to modify display of any media bundle. 

For example, suppose you don't want to display the created at date for the image files in the media library. Below are the steps you need to follow:

1. Open admin/structure/media/manage/image/display

2. Click on 'Media Library' above the page breadcrumbs.
  ![](/modules/media/modify_image_display.png)
3. Change the format for the Created field to Hidden.
4. Now open the media library \(admin/content/media\) and the created at field for the images media items won't be visible. 

You can also rearrange the display of the field and change the formats on this page.
