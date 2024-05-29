wagtail_meta
================

A library to manage meta-tags at runtime for your Wagtail site.

Allows for using context variables in a custom HTML meta tag, or the tag value content itself.

Quick start
-----------

1. Install the package via pip:

   ```bash
   pip install wagtail_meta
   ```

2. Add 'wagtail_meta' to your INSTALLED_APPS setting like this:

   ```
   INSTALLED_APPS = [
      # ...,
      'wagtail_meta',
      # ...,
   ]
   ```

3. Use the template tag in your base template
```html
{% load wagtail_meta %}
<!DOCTYPE html>
<html>
   <head>
       ...

       {% meta_tags %}
       {# Optionally call with model argument {% meta_tags settings.wagtail_meta.metatags.tags %} #}

       ...
   </head>
   <body>
       ...
   </body>
</html>
```