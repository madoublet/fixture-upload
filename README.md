# Fixture Upload

Fixture Upload is simple, drag-and-drop upload tool that allows you to upload files and images directly to Amazon S3.  Fixture Upload also features the and Pica JS, Cropper JS, and Caman JS libraries so that you can quickly resize, crop, and stylize your photos.

### Getting Started

Fixture Upload was built around a single plain JS class so that you can easily integrate it into the platform of your choice.

```
let el = document.querySelector('.app-upload');

let upload = new Upload(
    // upload el
    el, 
    // generate url
    function(file, done) {

        console.log('[debug] generate url');
        console.log(file);

        var url = "https://some-s3-url/";
        var method = "PUT"
        done(url, method);
    },
    // complete
    function(file) {},
    // error
    function(status, text) {}
);
```

### Learn more

See a demo and watch a video of Fixture Upload here: https://fixture.app/open-source/upload.html

### Acknowledgements

Fixture Upload would not be possible with these great Open Source projects.

http://camanjs.com/
https://github.com/nodeca/pica/blob/master/dist/pica.min.js
https://fengyuanchen.github.io/cropperjs/
https://codepen.io/joezimjs/pen/yPWQbd
