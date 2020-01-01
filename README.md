useful-scripts
==============

Small but useful scripts.

* Two related Ruby scripts that fit into my photography workflow: 
    * **tagsfromexposure** reads metadata from the [Exposure X4/X5 image editor](https://exposure.software), and applies [OSX Finder tags](https://www.macrumors.com/how-to/files-folders-tags-macos/) based on the metadata. Files flagged as "pick" get the `TAG_YES` tag applied; files with 2 or more stars get the `TAG_MAYBE` tag applied. This requires the `nokogiri` gem and the [`tag` commandline utility](https://github.com/jdberry/tag/), which you can `brew install`.
    * **albumfromtags** looks for images in the current directory with the `TAG_YES` or `TAG_MAYBE` tags, and generates a static HTML image gallery of those images. It relies on [sigal](https://sigal.saimon.org/en/latest/) and the `tag` commandline utility. You need to customise the `sigal.conf.py.example` file (to include your own name), put that file somewhere permanent, and update the path to it in the `albumfromtags` script. 

* **kickstart** is a tool to initialise an SVN repository for a new project. It creates a skeleton, checks it in, and checks out trunk into a new folder for you: `kickstart myproj "example project"` will create a new folder `myproj` with a trunk checkout. Edit the script to set your own repository location. I am aware of the irony of hosting this on github.
