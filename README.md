# AshfaqAliZardariOfficial.github.io


## Method
```
<script type="text/javascript">

        // Is a video link method.
        const isVideoLinkLink = (URL) => new Promise(resolve => {
            var v = document.createElement("VIDEO");
            try {
                v.onloadedmetadata = () => {
                    v.videoWidth > 0 && v.videoHeight > 0 ? resolve(true) : resolve(false);
                }
                v.error = () => {
                    resolve(false);
                }
            } catch (error) {
                resolve(false);
            }
            v.src = URL;

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
