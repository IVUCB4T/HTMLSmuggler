## HTMLSmuggler.html amd index.html both are some index.htmlfor online try.
# HTMLSmuggler is not an evil, it can be useful

### HTMLSmuggler File Builder
This is a self-contained HTML app, handy, supports Windows, Mac, Linux and mobile.

It adopts HTML smuggling technique, leverages HTML5 and JavaScript to embed encoded file into HTML file, when user runs the JavaScript code in browser, it decodes the embedded payload, which, in turn, assembles the target file on the destination device.

You can convert your file to HTML encoded format, with password protected, then use it as email attachment or file download from web.

![alt text]()

Download HTMLSmuggler.html from this repository or try it online

https://IVUCB4T.github.io/HTMLSmuggler


### HTMLSmuggler Tachnique

###### Use of JavaScript Blob
When working with Javascript, the file can be created by using a Javascript Blob. A Blob is a representation of payload.
```
  var bobject = new Blob([payload], {type: 'octet/stream'});
```

###### Using the URL.createObjectURL
It invoking the click action from within the Javascript, we mimic the user clicking on the link and starting the file download

```
  var hiddenobject = document.createElement('a');
  var url = window.URL.createObjectURL(bobject);
  hiddenobject.href = url;
  hiddenobject.download = targetfilename;
  hiddenobject.click();
```

Due to encoded patterns, no original file content passes through the network, bypassing email scanners, proxies and sandboxes.

As security admin, if you don't want user to bypass, you may fine tune the dection rule based on it's characteristics or simply block HTML file.



#HTMLSmuggler
#payload
#javascript
#pentest
#poc
#html
#smuggling
#tool
