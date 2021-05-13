# vanillaQuill_InlineStyleTest
Inline Style bug test with vanilla Quill JS

Bug occurs when QuillJS is loaded with text-indent style in the editor.

Open the HTML file, inspect the "Hello World!" line.  There will be some whitespace before the text and the text-indent style will have been removed from the tag that existed in the HTML when we loaded the file.

Uncomment the IndentAttributor javascript to use the Attributor.
Refresh the file in your browser.
Inspect the "Hello World!" line.  The text-indent style remains on the p tag, but there is also whitespace (a tab) inserted into the p element.  I don't believe this tab should have been inserted.
  
I believe the cause of the issue is in the clipboard.js matchStyles() function in QuillJS.
