# pyOCR-D

> Collection of OCR-related python tools and wrappers from the OCR-D team

## Requirements

* Python 3
* pip

If tesserocr fails to compile with an error:

```
 $PREFIX/include/tesseract/unicharset.h:241:10: error: ‘string’ does not name a type; did you mean ‘stdin’? 
       static string CleanupString(const char* utf8_str) {
              ^~~~~~
              stdin
```

This is due to some inconsistencies in the installed tesseract C headers. Replace `string` with `std::string` in `$PREFIX/include/tesseract/unicharset.h:265:5:` and `$PREFIX/include/tesseract/unichar.h:164:10:` ff.

## Installation

To install system-wide:

```sh
pip3 install -r requirements.txt
python3 setup.py install
```

To install to user HOME dir

```sh
pip3 install --user -r requirements.txt
python setup.py install --user
```


## See Also

* [OCR-D Specifications](https://github.com/ocr-d/spec)
