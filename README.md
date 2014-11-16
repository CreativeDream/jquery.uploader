jquery.uploader
===============

Simple jQuery Form Submit Plugin

Usage
-------
__HTML:__

Include the jquery.uploader Progressbar styles file in your html page.
~~~~ html
<link href="./css/jquery.uploader.css" type="text/css" rel="stylesheet" />
~~~~
Include the jQuery libraray and jquery.uploader script file in your html page.
~~~~ html
<script src="http://code.jquery.com/jquery-latest.min.js"></script>
<script src="./js/jquery.uploader.min.js"></script>
~~~~
Create a Form.
~~~~ html
<form action="" method="POST">
    <input type="text" name="text" value="Text Field" />
    <br>
    <inpu type="submit" name="submit" />
</form>
~~~~
__Javascript:__

The plugin is named "uploader" and can be applied to a form element. You will probably also specify some options while applying the plugin.
~~~ javascript
$('form').uploader({
      url: null, //URL
      data: null, //Data
      type: 'POST', //Type
      enctype: 'multipart/form-data', //Enctype
      cache: false, //$.ajax cache
      contentType: false, //$.ajax contentType
      processData: false, //$.ajax processData
      statusCode: {}, //$.ajax statusCode
      progress: false, //ProgressBar
      progressHTML: '<div class="uploader-progressbar"></div>', //ProgressBar HTML
      appendProgressTo : 'body', //ProgressBar append to element
      submitB: true, //Animate Submit button
      beforeSend: null, //beforeSend function(form){}, must return true to continue
      onSend: null, //onSend function(form){}
      onProgress: null, //onProgress function(percentage, progressbar, form){}
      success: null, //success function(data, form){}
      error: null, //success function(form){}
  })
  ~~~~
Features
-------
__trgigger Options:__

jQuery Manual Triggering $('form').trigger("option"):
* uploader.submit
* uploader.enable
* uploader.disable
* uploader.destroy

__attribute Options:__

Form element attributes:
* data-uploader | on, off, disabled
* data-validate | true, false
* data-uploader-beforeSend
* data-uploader-onSend
* data-uploader-success
* data-uploader-error

License
-------
> Licensed under <a href="http://opensource.org/licenses/MIT">MIT license</a>.
