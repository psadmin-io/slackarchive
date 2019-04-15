[![Build Status](https://travis-ci.org/psadmin-io/slackarchive.svg?branch=master)](https://travis-ci.org/psadmin-io/slackarchive)

# slackarchive

Process to create the slackarchive.aws.psadmin.cloud site.

1. Currently, request a manual export of the Slack Channels and download the .zip files. (In the future, look to automate the export.)
1. Unzip the download.
1. Download the `slack2html.php` script

        curl -o slack2html.php https://gist.githubusercontent.com/iversond/01c5a80e0a85d040229be50761b652e1/raw/6ea53ecfb936f4f0fbbcbb74bb7b6db5030ec64b/gistfile1.txt

1. Create the HTML files

        cd <export folder name>
        php ./slack_archive.php
        cd ../slack2html/html

1. Upload HTML files to S3 bucket. Set permission to public read.
```


## TODO

Possible repo to export public channels: https://github.com/zach-snell/slack-export
    
    python slack_export.py --token $SLACK_TOKEN --publicChannels

