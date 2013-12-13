## Description

![home page](http://f.cl.ly/items/140I3u1x1n1k230v053y/screenshot1.png)

![gallery page](http://f.cl.ly/items/3c1h3H321m443l0P2Q2F/screenshot2.png)

I created this [Statamic](http://statamic.com/ "Home | Statamic") theme to make a mostly automated photo gallery for my family. My Eye-Fi SD card in the camera uploads the "best" shots to the FTP server automatically (putting the images into dated folders). Then, all I need to do is create a quick markdown file giving the gallery a thumbnail image and description (text expander makes quick work of this, or it's easy enough from the admin panel). 

Basically, I wanted the site to be responsive, clean, and put the focus on the images, and make it easy to download high-res versions (for printing pics of grandchildren). 

I'm no web designer, so I cobbled this site together with code from around the web, including:

* [videojs](http://www.videojs.com/) - for responsive HTML5 videos in multiple formats for parents on Windows
* [magnific-popup](http://dimsemenov.com/plugins/magnific-popup/ "Magnific Popup&#58; Responsive Lightbox & Dialog Script") - a responsive lightbox with lots of different configuration options
* Nathan Rohler's [responsive image grid code](http://www.dwuser.com/education/content/creating-responsive-tiled-layout-with-pure-css/ "Creating a Responsive Tiled Photo Gallery with Pure CSS - DWUser.com Education Center")
* Ali Jafarian's [responsive image grid code](http://alijafarian.com/responsive-image-grids-using-css/ "Responsive Image Grids Using CSS Tutorial | alijafarian.com")

Thanks to all these designers for creating and sharing this code! Thanks also to [Erik Hess](http://twitter.com/themindfulbit) for encouraging me to try Statamic when I was thinking I might have to learn Python or Ruby and use Pelican or Jekyll. This turned out to be surprisingly do-able for someone who really only had a basic grasp of HTML/CSS and no experience with templating and variables.

If you're a web designer and are interested in this concept, I'd love to hear suggestions or get pull requests to make this better in any way. It's just a hobby for me, so I'm sure this is pretty hack-y and I'd love for it to be more professional.

## Settings

1. Set appropriate variables in the `/_config/settings.yaml` file:    
`_site_url:` enter your root url   
`_theme: familyphotos`   
`_transform_destination: /assets/img/trans/`

## Use

### For images

1. Add images to `/assets/img/` in dated folders
2. Create new posts in `_content/1-galleries/`
	* Use the admin panel or create a `.md` file named with date and slug (follow sample content)
3. Make sure the `gall:` YAML variable points to the same date as the image gallery folder
4. Choose one of the images in the gallery as the thumb and enter into the `thumb:` YAML variable

### For video

*At this point, only one video per page*

1. Add video files (mp4 and/or ogg) to `/assets/video` in dated folders
2. Create new posts in `_content/1-galleries/`
	* Use the admin panel or create a `.md` file named with date and slug (follow sample content)
3. Make sure the `gall:` YAML variable points to the same date as the video  folder
4. Create a thumbnail for the video and upload it to the same directory as the video files and enter the name into the `thumb:` YAML variable
5. Enter the video's filename (without the file extension) into the `filename:` YAML variable