# 图标尺寸详解

根据手机的像素密度的不同, 图片大小大致可以分为3类

* 1x图: 也称为基准图，是指在标准像素密度 (通常为160dpi) 的设备上显示正常大小的图片。例如，在Android开发中，1x图对应mdpi (medium density pixel per inch) 密度设备。

* 2x图: 也称为高清晰度图，是相对于1x图来说分辨率提高一倍的图片。它主要用于高像素密度 (通常为320dpi) 的设备上显示，以保持图片在高像素密度屏幕上的清晰度。在Android开发中，2x图对应hdpi (high density pixel per inch) 密度设备

* 3x图: 也称为超高清晰度图，是相对于1x图来说分辨率提高两倍的图片。它主要用于非常高像素密度 (通常为480dpi或更高) 的设备上显示。在iOS开发中，3x图主要用于iPhone Plus系列和部分iPad设备。

* 通过提供不同分辨率的图片资源，可以确保应用程序在不同像素密度的设备上都能够以最佳质量进行显示，并避免因拉伸或缩放导致的模糊或失真现象。开发人员可以根据不同设备的像素密度，为每个分辨率提供相应的图片资源，并在应用程序中动态加载适合当前设备的图片。

同一张图片的1x、2x和3x主要区别在于分辨率和显示效果。

* 分辨率：1x图是基准图，其分辨率适用于标准像素密度（通常为160dpi）的设备。2x图相对于1x图来说， 分辨率提高一倍，适用于高像素密度（通常为320dpi）的设备。3x图相对于1x图来说，分辨率提高三倍，适用于非常高像素密度（通常为480dpi）的设备。

* 显示效果：由于不同像素密度的设备具有不同数量的物理像素，使用不同分辨率的图片可以保持在各自设备上的清晰度和细节。当使用低分辨率的图片在高像素密度设备上显示时，可能会出现模糊或失真情况。而使用对应分辨率的图片可以保持更好的显示效果。

举个例子，假设有一张100px × 100px的图片：

* 在标准像素密度设备上（1x），该图片将以原始大小（100px × 100px）进行显示。

* 在高像素密度设备上（2x），如果只使用1x图，则该图片将被拉伸至200px × 200px进行显示，导致模糊或失真。但如果使用对应的2x图，则该图片将以原始大小（100px × 100px）进行显示，并保持清晰度。

* 在非常高像素密度设备上（3x），如果只使用1x或2x图，则该图片将被拉伸至300px × 300px进行显示，导致模糊或失真。但如果使用对应的3x图，则该图片将以原始大小（100px × 100px）进行显示，并保持清晰度。

因此，在开发移动应用时，为了适应不同像素密度的设备并提供最佳显示效果，建议同时提供1x、2x和3x三种分辨率的图片资源，并在应用程序中根据设备的像素密度动态加载适合的图片。

# ios桌面图标

| 图片尺寸           | 图片命名                         | 图片描述                | 图片存放目录                   |
|:---------------|:-----------------------------|:--------------------|:-------------------------|
| 20 x 20        | Icon-App-20x20@1x.png        | 20 x 20的1x图         | AppIcon.appiconset       |
| 40 x 40        | Icon-App-20x20@2x.png        | 20 x 20的2x图         | AppIcon.appiconset       |
| 60 x 60        | Icon-App-20x20@3x.png        | 20 x 20的3x图         | AppIcon.appiconset       |
| 29 x 29        | Icon-App-29x29@1x.png        | 29 x 29的1x图         | AppIcon.appiconset       |
| 58 x 58        | Icon-App-29x29@2x.png        | 29 x 29的2x图         | AppIcon.appiconset       |
| 87 x 87        | Icon-App-29x29@3x.png        | 29 x 29的3x图         | AppIcon.appiconset       |
| 40 x 40        | Icon-App-40x40@1x.png        | 40 x 40的1x图         | AppIcon.appiconset       |
| 80 x 80        | Icon-App-40x40@2x.png        | 40 x 40的2x图         | AppIcon.appiconset       |
| 120 x 120      | Icon-App-40x40@3x.png        | 40 x 40的3x图         | AppIcon.appiconset       |
| 120 x 120      | Icon-App-60x60@2x.png        | 60 x 60的2x图         | AppIcon.appiconset       |
| 180 x 180      | Icon-App-60x60@3x.png        | 60 x 60的3x图         | AppIcon.appiconset       |
| 76 x 76        | Icon-App-76x76@1x.png        | 76 x 76的1x图         | AppIcon.appiconset       |
| 152 x 152      | Icon-App-76x76@2x.png        | 76 x 76的2x图         | AppIcon.appiconset       |
| 167 x 167      | Icon-App-83.5x83.5@2x.png    | 83.5 x 83.5的2x图     | AppIcon.appiconset       |
| 1024 x 1024    | Icon-App-1024x1024@1x.png    | 1024 x 1024的1x图     | AppIcon.appiconset       |

# android桌面图标

| 图片尺寸          | 图片命名                  | 图片存放目录                 |
|:--------------|:----------------------|:-----------------------|
| 48 x 48       | ic_launcher.png       | mipmap-mdpi            |
| 72 x 72       | ic_launcher.png       | mipmap-hdpi            |
| 96 x 96       | ic_launcher.png       | mipmap-xhdpi           |
| 144 x 144     | ic_launcher.png       | mipmap-xxhdpi          |
| 192 x 192     | ic_launcher.png       | mipmap-xxxhdpi         |

# ios 启动页图片

| 图片尺寸          | 图片命名                  | 图片存放目录                 |
|:--------------|:----------------------|:-----------------------|
| 720 x 1280    | LaunchImage.png       | LaunchImage.imageset   |
| 1080x 1920    | LaunchImage@2x.png    | LaunchImage.imageset   |
| 1440 x 2560   | LaunchImage@3x.png    | LaunchImage.imageset   |

# android 启动页图片

| 图片尺寸          | 图片命名                  | 图片存放目录                 |
|:--------------|:----------------------|:-----------------------|
| 320 x 480     | launch_image.png      | mipmap-mdpi            |
| 480 x 800     | launch_image.png      | mipmap-hdpi            |
| 720 x 1280    | launch_image.png      | mipmap-xhdpi           |
| 1080 x 1920   | launch_image.png      | mipmap-xxhdpi          |
| 1440 x 2560   | launch_image.png      | mipmap-xxxhdpi         |
