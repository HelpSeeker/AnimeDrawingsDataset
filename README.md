Anime Drawings Dataset
======================

A dataset for 2D pose estimation of anime/manga images.  This repository contains code to:

  * Download images from the Internet and process them.
  * Generate HTML files that allow the user to view the dataset.

Dependencies
------------

  * The Ruby programming language.
  * The following Ruby packages. (You only need to have the first one installed.)
    * `bundler` (for installing the following three packages)
    * `rake` (for automation)    
    * `nokogiri` (for HTML processing)
    * `mechanize` (for interaction with web pages)
  * ImageMagick
    * You should be able to run the `convert` command from the shell.

Preparing the Dataset
---------------------

First, please clone the dataset into a directory of your choice.  Then, change into the directory of the repository.  At this point, you should have (1) the Ruby language, (2) the `bundler` package, and (3) ImageMagick installed in your system.

The next step is to install other Ruby packages.  Run:

    bundle install

Then, run:

    rake build

The above command will download all the images and process them.  This can take some time, so sit back, relax, and wait.

After the above command finishes, you can browse the dataset by viewing the HTML page `index.html` in the root of the repository.

Where Are the Data?
-------------------

The images are located in the `data/images` directory.  The joint positions are located in the following files:

  * `data/data.json` contains all the 2,000 examples.
  * `data/train.json` contains the 1,400 training examples.
  * `data/val.json` contains all the 100 validation examples.
  * `data/test.json` contains all the 500 test examples.

Some joint names are a little counter-intuitive:

  * `arm_left` and `arm_right` are the shoulder joints.
  * `leg_left` and `leg_right` are the hip joints.
  * `tiptoe_left` and `tiptoe_right` are the tips of the shoes or feet (if the character does not wear shoes).

Acknowledgement
---------------

This dataset would not have been possible without volunteers who helped us annotated the pictures.  Thank you very much!
