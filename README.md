# NAME

IMMUSE -- image conversion and manipulation utility

# SYNOPSIS

    immuse -r 90 -a -f gif *.jpg
    immuse -i jpeg file.bin -f png -o file.png
    immuse -x 800 -y 600 -q 77 ../*.jpg

# INTRODUCTION

IMMUSE is a command line utility for image conversion and manipulation.
IMMUSE is written in Perl and uses Imager perl module.
IMMUSE offers the following image manipulations:

    * format conversion (all supported by local Imager installation)
    * scaling/resizing
    * stretching
    * aspect-preservig single dimension scaling/resizing
    * flipping, horizontal and vertical
    * rotation, CW. CCW and by EXIF information
    * grayscale conversion

IMMUSE is designed to work on many files in one run but can be used on single 
file with optional destination filename change.

# QUICK USAGE HELP

usage: immuse <options> [input-files]

options:
    -o output-file-name  -- sets output file, works only for single input file
    -f output-format     -- sets output file format (i.e. JPEG, GIF, etc.) 
    -i input-format      -- sets input  file format (i.e. JPEG, GIF, etc.) 
    -x width             -- sets output image width in pixels (keeps aspect!)
    -y height            -- sets output image width in pixels (keeps aspect!)
    -x width%            -- sets output image width in percents (keeps aspect!)
    -y height%           -- sets output image width in percents (keeps aspect!)
    -h                   -- flip image horizontally 
    -v                   -- flip image vertically   
    -g                   -- convert image to grayscale
    -r degrees           -- rotate by degrees CW, negative for CCW
    -r exif              -- rotate by EXIF info
    -q quality           -- output quality in percents (if applicable)
    -a                   -- always overwrite files (WARNING!)
    -n                   -- never  overwrite files (skip, existing)
    --        -- end of options

notes:

# NOTES

    * "-i list" or "-f list" will list supported file formats
    * if both -x and -y specified, aspect will not be kept!
    * use "-x nnnn -y 100%" to stretch horizontally
    * use "-x 100% -y nnnn" to stretch vertically
    * options cannot be grouped: -fd is invalid, correct is: -f -d

# GITHUB REPOSITORY

    https://github.com/cade-vs/immuse

    git clone git://github.com/cade-vs/immuse.git

# AUTHOR

    Vladi Belperchinov-Shabanski "Cade"

    <cade@bis.bg> <cade@cpan.org> <shabanski@gmail.com>

    http://cade.datamax.bg
    

    https://github.com/cade-vs

## EOF
