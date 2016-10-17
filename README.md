# Tesseract on Heroku

This app is written in Python and using Flask web framework.

Based on Maggioni's [secret-harbor app] (https://github.com/matteotiziano/secret-harbor).

# Set up

Before deploying app to Heroku, run:

```
heroku buildpacks:set heroku/python
``` 
```
heroku buildpacks:add https://github.com/lnguyen46/heroku-buildpack-tesseract.git
```
# Link:

This app is hosted on: https://tesseract-with-flask-python.herokuapp.com

# How it works:

1. Flask get photos by using ```request.files```
2. Run ```subprocess```:

  ```$ tesseract input_file output_file -l eng ```
  
3. Read ```output_file``` and hold value with variable.
4. Delete ```output_file``` and return value.

# License:

MIT.

