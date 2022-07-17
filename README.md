# [IsUrlAValidVideoURL](https://ashfaqalizardariofficial.github.io/IsUrlAValidVideoURL.github.io/) 
by ***Ashfaq Ali Zardari***  
A native JavaScript programming code to know is Link/URL a valid video Link/URL that can be played.


## Method
```
<script type="text/javascript">

       // Is a video link method.
        const isVideoLinkLink = (URL) => new Promise(resolve => {
            var v = document.createElement("VIDEO");
            try {
                v.onloadedmetadata = () => {
                    resolve(v.videoWidth > 0 && v.videoHeight > 0);
                }
                v.onerror = () => {
                    resolve(false);
                }
            } catch (error) {
                resolve(false);
            }
            var isURL = new RegExp('^(https?:\\/\\/)?' + // protocol
                '((([a-z\\d]([a-z\\d-]*[a-z\\d])*)\\.)+[a-z]{2,}|' + // domain name
                '((\\d{1,3}\\.){3}\\d{1,3}))' + // OR ip (v4) address
                '(\\:\\d+)?(\\/[-a-z\\d%_.~+]*)*' + // port and path
                '(\\?[;&a-z\\d%_.~+=-]*)?' + // query string
                '(\\#[-a-z\\d_]*)?$', 'i'); // fragment locator
            if (!!isURL.test(URL)) {
                v.src = URL;
            } else {
                resolve(false);
            }
        })
</script>
```

## Usage
```
<script type="text/javascript">
// Sample URLs.
        var videoURLs = [
            "http://c39.pcloud.com/cBZaX75K1ZuNXI2PZZZxoHtr7ZQ5ZZanFZkZlyLPFZz5ZcZRVZrzZ9XZI5Z70ZW5ZVVZxZHJZJXZUFZMJZ4NfPXZsHTjKtWRhlFl8urEbyXTffdEzDDV/Signature_InsertShow_With_WYSIWYG_Editor_07_July_2021_Wed.mp4"
            , "https://file-examples.com/storage/fecadf937e62d089e9bc0c7/2017/11/file_example_MP3_2MG.mp3"
            , "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
            , "http://techslides.com/demos/sample-videos/small.webm"
            , "http://techslides.com/demos/sample-videos/small.ogv"
            , "http://techslides.com/demos/sample-videos/small.mp4"
            , "http://techslides.com/demos/sample-videos/small.3gp"
            , "https://drive.google.com/uc?export=download&id=1MeEnp4I32vGmDfZbBTNRDa0jEtk07fOr"
            , "https://filesamples.com/samples/video/3gp/sample_640x360.3gp"
            , "https://vimeo.com/726789599"
            , "http://www.youtube.com/watch?v=PVfJnltHIM4"
            , "http://www.youtube.com/watch?v=bYfAyv8p91Y"
        ];

        // Usage.
        var Sr = 0;
        videoURLs.forEach(videoURL => {
            isVideoLinkLink(videoURL).then(isVideoLink => {
                // The "isVideoLink" param variable type is boolean, if true means the link is a video link otherwise false.

                // Commit or remove the below code, This was for testing purposes only.
                Sr++;
                var p = document.createElement('p').innerHTML = `${Sr}) ${isVideoLink} ${videoURL}`;
                document.body.append(p, document.createElement('br'));
            })
        });

    </script>
```
## Contact and Supporting Info
Feel free to contact me on <a href="mailto:ashfaqalizardariofficial@gmail.com" target="_blank" title="ashfaqalizardariofficial@gmail.com"><img src="https://ssl.gstatic.com/ui/v1/icons/mail/rfr/logo_gmail_lockup_default_1x_r2.png" alt="ashfaqalizardariofficial@gmail.com" width="70" /></a>  
  
  <a href="https://paypal.me/ashfaqalizardari247?country.x=CA&locale.x=en_US" target="_blank" title="paypal.me/ashfaqalizardari247"><img src="https://www.paypalobjects.com/paypal-ui/logos/svg/paypal-color.svg" alt="PayPalMe" width="160" /></a>    <a href="https://www.buymeacoffee.com/ashfaqalizardari" target="_blank" title="buymeacoffee.com/ashfaqalizardari"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" width="160" /></a>

