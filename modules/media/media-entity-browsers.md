# Media entity browsers

Media module uses [entity\_browser](/modules/entity_browser/intro.md) to manage media select modals. List of the available entity browsers can be found at admin\/config\/content\/entity\_browser. By default the media module comes with three entity browsers:

* **Gallery media library:** It provides an entity browser to select media items for creating a new gallery.
* **Media embed:** It provides an entity browser for selecting media files to embed in the wysiwyg editor.
* **Media library:** It provides a general entity browser with a media library which can be used for custom content types.

![](/modules/media/entity_browsers.png)

## Customizing entity browser

**Adding more widgets to the entity browser**

While selecting the media items for the gallery, an entity browser called gallery\_media\_library is used. Suppose in this modal you want to add a tab for uploading document files. You need to add an entity browser widget for it. You need to follow these steps:

1. Go to Configuration &gt; Entity Browsers
2. Click on Edit for gallery\_media\_library
3. Go to the widgets section
4. In the 'add widget plugin' dropdown, select 'Entity form'
5. Fill in the appropriate details and click on Finish.

![](/modules/media/add_document_widget.png)

