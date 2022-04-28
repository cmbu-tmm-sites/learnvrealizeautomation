---
title:  "Publishing Preserved Artifacts"
img: "codestream-tile.png"
externalUrl: "https://learncodestream.github.io/learn-in-5/publishing-preserved-artifacts/"
---
With the CI task in a Code Stream Pipeline, it’s possible to Preserve Artifacts - any file that you want to persist beyond the lifetime of a Pipeline Execution can be added to the Preserve Artifacts field. These preserved artifacts are stored on the Shared Path on the Docker Host , which you can access later using the file path specified in the CI task outputs. One of the issues with this is that the Shared Path is also where the pipeline execution logs are kept, which may contain sensitive information if you’re not using Secret Variables , and to deliver a preserved file to an end user you may need to grant SSH access to your host - not ideal.