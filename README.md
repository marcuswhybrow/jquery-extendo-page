
Usage
=====

The plugin should only be applied to `a` elements, and requires 2 arguments:

1. findSelector - A string containing a jQuery selector, specifying the elements you wish to get.
2. targetSelector - A string containing a jQuery selector, specifying the element to attach the found elements to.

Options
-------

* spinnerImage (default: null) - The URL of an image to display whilst waiting.
* recursiveLink (default: null) - A string containing a jQuery selector specifying the next link to follow (usually the same selector to which this function was applied).
* message (default: 'There are no more posts') - A message to display when the recursive link is eventually not found (thus no more pages of items are available).
* newText (default: '+ More Posts') - New string to replace the existing links text with, for a more authentic meaning.

For example:

    $('#older-posts a').extendoPage('#post-list .post', '#post-list', {
        spinnerImage: '/path/to/ajax-loader.gif',
        recursiveLink: '#older-posts a'
    });