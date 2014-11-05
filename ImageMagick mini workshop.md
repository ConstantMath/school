# Imagemagick

### Installation
apt-get update
apt-get imagemagick

brew update
brew install imagemagick

### Some commands
convert image.jpg image.png
convert *.jpg -colors 2  export/%d.png
convert *.jpg -resize 400%  export/%d.png
convert *.jpg -resize 400% -colors 2  export/%d.png
convert *.jpg anim.gif

# FFmpeg

### Installation
apt-get ffmpeg
brew install ffmpeg

### Some commands
mkdir seq

ffmpeg -i movie.mov seq/%d.png

mkdir resized

convert seq/{1..25}.png -resize 20% resized/%d.png

convert -delay 3 -loop 0 resized/*.png anim.gif
