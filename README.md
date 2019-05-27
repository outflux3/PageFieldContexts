# PageFieldContexts

This module enables you to switch the template/fieldgroup for the currently edited page based on a page field value.

## Table of Contents

- [Benefits](#benefits--uses)
- [Installation](#installation)
- [Usage](#usage--configuration)
- [Support](#support)
- [Contributing](#contributing)


## Benefits & Uses

As opposed to using built in field visibility or dependencies, you can change anything that is context enabled, such as:

- Descriptions & Notes
- Editor layout, position of fields
- Visibility of any field
- Required status of a field

This can improve the user friendliness of your admin edit pages by hiding fields that are irrelevant based on another field's value, changing descriptions, or altering the layout, order, or columns of the editor.

One example might be if you had a Page Reference field for a "Widget Type". Say you are using a single template for your widgets, and that template has all of the fields needed to configure any widget, but some fields are specific only to certain widgets. You could duplicate the widget template and then setup the fieldgroup switch to that template based on the selected option.

Why not just change the template itself?

The ability to switch the fieldgroup based on a Page Reference field's value is similar to a Repeater Matrix's ability to change the matrix type. Two obvious reasons why using the select field to change the fieldgroup instead of template change are (1) The user's access level may prohibit them changing the template on a page, and (2) changing the template for the page would require more training, going to a different tab, and a lot of other configuration settings to ensure they can only select certain templates. 

## Installation

Upload or install from Modules directory.  

## Usage & Configuration

Once installed, on any Page Reference field, you will be able to activate the Page Field contexts (checkbox). Once activated, there is a textarea to enter your parameters. The parameters are 1 per line, and look like this:

[Enable on Template], [Page ID], [template to trigger]

So here is an example, and this is setup on a widget_type field, which is a Page Reference field where the user selects the type of widget they are configuring.

``widget,1677,pfc-widget-type-image``

this line is saying:

"On any page editor using **widget** template, if this field (widget_type) has a value of **1677** (image), switch the template to **pfc-widget-type-image**."

So what this is doing is allowing us to have a custom subset of fields shown on the editor when the user selects the image type of widget, and now we can eliminate irrelevant fields, change what is required, alter field descriptions etc.

One thing that is recommended is to keep your context versions of any template in sync with the main template in terms of the fields present, so it is better to change the visibility of fields, rather than removing them from the fieldset, so that it is easier to compare later on if you add any fields to the main template. Possibly in the future there could be some way of auto-syncronizing the master template with the context modded versions...


## Support

URL coming soon, for PW support forum thread.

## Contributing

Please contribute using [Github Flow](https://guides.github.com/introduction/flow/). Create a branch, add commits, and [open a pull request](https://github.com/outflux3/PageFieldContexts/compare/).
