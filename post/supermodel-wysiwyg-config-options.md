---
title: Supermodel WYSIWYG config options
date: 2016-05-08
tags:
  - supermodel
  - wysiwyg
  - config
---

Configuration options for WYSIWYG fields in Supermodel. To add config for a specific field you will need to create a file (.jsp) inside `/WEB-INF/supermodel-local/tinymce/config/`.
File names need to match the field name, but lowercased, and should live inside a subfolder with the same name as the parent object. e.g. if you want to add configuration for a 'content' field inside a `block.text` object, then the structure would look like:

~~~shell
config/
├─ block.text/
   ├─ content.jsp
~~~

Inside the file you can add your configuration:

~~~html
<%@include file="/WEB-INF/templates/frag/global.jspf" %>
tinyMCEConfig.content_css = "<sm:static path="/static/css/admin/page-content.css" />";
tinyMCEConfig.height = "250";
tinyMCEConfig.theme_advanced_blockformats = "p,br";
tinyMCEConfig.theme_advanced_buttons1 = "styleselect,|,bold,italic,|,link,unlink";
tinyMCEConfig.valid_elements = "p[class],em/i,strong/b,a[href|target],br";
tinyMCEConfig.theme_advanced_statusbar_location = "none";
~~~

Ideally you will want to set the `tinyMCEConfig.valid_elements` to only allow elements that you have provided styling for.
The `theme_advanced_buttons1` values determind which buttons show up on the WYSIWYG toolbar, and the most common values are:

~~~
bold, italic, underline, strikethrough, justifyleft, justifycenter, justifyright, justifyfull, bullist, numlist, outdent, indent, cut, copy, paste, undo, redo, link, unlink, image, cleanup, code, hr, removeformat, formatselect, styleselect, sub, sup, blockquote,
~~~

You can also turn off all buttons by passing in an empty &ldquo;&rdquo; string. Note that this will hide the buttons but not the bar, so to remove that you&rsquo;ll also need to add some javascript into the bottom of the config file:

~~~js
if ( $('#supermodel-custom-admin-styles').length == 0 ) {
	var adminStyles = '';
	adminStyles += '#field_fieldCode_tbl tr.mceFirst { display:none; } #field_fieldCode_ifr, table#field_fieldCode_tbl.mceLayout { height: 54px !important; }';
	
	$('body').append('<style id="supermodel-custom-admin-styles">'+adminStyles+'</style>');
}
~~~

Where &ldquo;fieldCode&rdquo; needs to be replaced by the relevant ID in the markup for the WYSIWYG wrapper. Adjust the height values to suit based on the font size etc.

Check the [TinyMCE docs](http://archive.tinymce.com/wiki.php/Configuration3x:valid_elements) for information about the `valid_elements` options.
