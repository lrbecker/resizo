Resizo
=======
Resizo is a simple command line interface for resizing images from the command line using the FreeImage + ImageScience libraries.

## Required Libraries/Frameworks
- Ruby 1.8.6+ 
- FreeImage

## Required Gems
- Image Science
- RubyInline

## Installation 
Run these commands to get the dependencies needed:
Note: You could compile FreeImage without Homebrew

        sudo brew install FreeImage
        sudo gem install image_science RubyInline

Or try out the install.sh (still a bit rough)
        
        ./tools/install.sh


## Usage example
### Parameter style
        ./bin/resizo -o ~/Pictures/photos -d ~/Pictures/photos_cropped -h 450 -w 450

### YAML config style
        ./bin/resizo -c sample-config.yml

## Gotchas
If using resizo with parameters the paths must be the full path, whereas using a config file to be relative. eg.

        (params) ~/Users/full/path/to/images

        (config) path/to/images

## Options
        Usage:
            resizo [options]
  
            where [options] are:
              --dest, -d:   Destination image path
              --orig, -o:   Original image path
              --width, -w <i>:   Desired width of image
              --height, -h <i>:   Desired height of image
              --config, -c <s>:   Parse a yaml configuration file
              --version, -v:   Print version and exit
              --help, -e:   Show this message

