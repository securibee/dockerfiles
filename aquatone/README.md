Dockerfile to install [aquatone](https://github.com/michenriksen/aquatone), using [Golang](https://golang.org/) and [headless Chromium](https://www.chromium.org/getting-involved/download-chromium). I tried to keep the image size as small as possible.

Run the command below to execute `aquatone` and output it to `~/aquatone` or a different directory of your choice.

```
echo 'www.google.com' | docker run -v ~/aquatone:/output --rm -i aquatone -out /output
```