# sphinx-thebe fork

This is a fork of the sphinx-thebe project, in an attempt to make it work with aplus

Goal of the fork: make it very easy for a teacher to make this work with aplus

# Changes to shpinx-thebe code
- Old python and sphinx syntax used on aplus servers / in the testing containers
  - add_js_file vs add_javascript
  - add_css_file vs add_stylesheet
  - ptyhon format strings
- Changing hardcoded binderhub link
  - Right now it's just hardcoded again
- Added div around button to make it stylable

# Changes needed in aplus repo
- Edit the template file (and include it in the sphinx config) to use the javascript
  - Add the needed javascript files manually to template
  - Create a file containing the string-form javascript ("extra-js")
  - Remember to set data-aplus=yes here.
- Add sphinx-thebe and a path to it into conf.py

# Changes I would like
- Attach button automatically to each box, showing if kernel is active
- Translate/localize the messages given while launching
- Using gitlab repository
- Submitting code
- Injecting code saved somewhere else (aplus database, browser storage)
- Adding the data-aplus attribute in the add_js_file function (once that works on aplus servers&docker)