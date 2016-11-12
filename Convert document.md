## unoconv
#### http://dag.wiee.rs/home-made/unoconv/
#### https://wiki.debian.org/LibreOffice
#### unoconv converts between any document format that OpenOffice understands. It uses OpenOffice's UNO bindings for non-interactive conversion of documents. Supported document formats include Open Document Format (.odt), MS Word (.doc), MS Office Open/MS OOXML (.xml), Portable Document Format (.pdf), HTML, XHTML, RTF, Docbook (.xml), and more.
###### pdf -> txt (pdftotext) 
```
sudo apt-get install poppler-utils
```
###### pptx,docx,xlsx -> txt (unzip) 
###### ppt,doc,ppt -> pdf (unoconv)
```
sudo apt-get install unoconv
```
