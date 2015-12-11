# Field Formatter

[Field Formatter](https://www.drupal.org/project/field_formatter) module adds formatters for entity reference fields to output only a specific field or field value using a specific formatter w/o needing to configure media view mode and configuring it to display properly. This module provides two formatters: *Field formatter with inline settings* and *Field formatter from view display*.

## Installation

1. Download [Field Formatter](https://www.drupal.org/project/field_formatter) from [GitHub](https://github.com/drupal-media/field_formatter).
2. Install it in the [usual way](https://www.drupal.org/documentation/install/modules-themes/modules-8).

## Usage

1. Create entity reference field
  * On `admin/structure` choose **Content types**

    ![Step 1](images/step_1.png)
  * Choose content type on which you want to use entity reference field, for example: *Article*, and click **Manage fields**

    ![Step 2](images/step_2.png)
  * Click **+ Add field**

    ![Step 3](images/step_3.png)
  * From **References** menu choose **Other**, fill the *Label* and click **Save and continue**

    ![Step 4](images/step_4.png)
  * Choose **Type of item to reference**, for example: *Content*, and click **Save field settings**

    ![Step 5](images/step_5.png)
  * Select which content types you want to reference in **Reference type section**, for example: *Article*, and click **Save settings**

    ![Step 6](images/step_6.png)
2. Choose field formatter for your entity reference field
  * On your content type open Manage display (in our case *Article*), on `admin/structure/types/manage/article/display`

    ![Step 7](images/step_7.png)
  * Choose which formatter you want to use on your entity reference field, *Field formatter with inline settings* or *Field formatter from view display*

    ![Step 8](images/step_8.png)
  * In formatter settings in *Field name* choose field you want to display from referenced entity in your article

    ![Step 9](images/step_9.png)
  * If you use *Field formatter from view display* beside field you must choose *View mode* also
  * Click **Update** and then **Save**

    ![Step 10](images/step_10.png)
3. Create a new node (in our case *Article*) with entity reference field
  * In `admin/content` click **+ Add content**

    ![Step 11](images/step_11.png)
  * Choose node to create (in our case *Article*)

    ![Step 12](images/step_12.png)
  * Fill *Title* and all the other fields, for your entity reference field choose entity (or in our case *Article*) you want to reference and click **Save and publish**

    ![Step 13](images/step_13.png)
  * The chosen field from referenced entity is displayed on the saved article page
