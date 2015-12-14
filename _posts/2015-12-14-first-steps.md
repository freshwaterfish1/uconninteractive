---
layout: post
title: First Steps
published: true
---



# Why Unreal 4?
First off, it looks great and for this project the better I can get it to look, the bigger impact it will have on players. Since this game is meant to demo UConn just as much as the Oculus, I want to have the “wow” factor and form what I have seen this engine delivers on that. Second, I have made a VR game in Unreal 4 before and while it was right when the DK2 came out, it still ended up being a pretty solid game. However I have since seen all the VR / HMD updates Unreal 4 has implemented and compared to other major game engine they seem to be the most up to date. Finally, I have experience with the engine. Just the fact I can navigate and find my way around 2/3rds of the time is a huge boon, and will cut down on the learning curve a lot leaving me more time to develop.
Much of this project will be exploring the beauty of the engine, rather than code or intense game mechanics. While I do plan to have small interactions in each scene, this isn’t the main goal of the project. I hope that can optimize a few scenes and get as close to photo realistic as possible in the Oculus. Once I’m happy with the performance and the immersion I will start to work on game mechanics. For now I feel much of the game mechanics will come to me as I experiment in the rift as see what “feels” cool – since much of what works in traditional media translates very differently once in virtual reality.


# Agisoft PhotoScan – the savior
Agisoft PhotoScan is software that creates models from many photos taken of a specific object. It then textures those models with the pictures, this process is called [Photogrammetry]( https://en.wikipedia.org/wiki/Photogrammetry). Basically, it’s magical. Instead of having to model everything, especially complex things such as the Jonathan the Husky statue, or various other structures around campus that would be time consuming to model.
The downsides to the software is that it’s _very_ taxing on a computer, and creates _many_ unnecessary polygons which doesn’t make it idea for game development. However some it seems that it can be cleaned up in ZBursh according to [this]( https://www.unrealengine.com/blog/creating-assets-for-open-world-demo) blog post by Harrison Moore.
# Taking the pictures
![ Me taking photos of Jonathan]({{ site.baseurl }}/images/Screenshots/TakingFootage.PNG " Me taking photos of Jonathan ")
I took 164 pictures with a Canon EOS 5D Mark III with the following settings:
F-stop | Exposure | ISO |Focal Length
--- | --- | --- | --- 
f/5.6 | 1/160 sec. | ISO-100 | 21 mm
![ Folder of photos I took of Jonathan]({{ site.baseurl }}/images/Screenshots/photostaken.PNG " Folder of photos I took of Jonathan ")
I ended up taking a few more pictures than I think where needed, plus I didn’t have the right lens for the camera at the time. I was using a bit of a wide angle lens which made taking the pictures easier, but I feel challenged the software, and led to the long load times. In the future I might go with a tripod setup, and definitely a different lens.

# Rendering Jonathan
Rendering in Agisoft Photoscan is split into 4 processes, the point cloud, the dense point cloud, the model, and the texturing of said model. 
## Point Cloud
![ Jonathan point cloud in Agisoft]({{ site.baseurl }}/images/Screenshots/pointcloud.PNG " Jonathan point cloud in Agisoft ")
For this, the software builds a rough could of points for you to get a feel of what’s going on in the scene. After this is done, (took about 3 hours) you can limit how much will be rendered on the next steps. The idea here is to “but away” as much as possible to speed up the process for the longer renders.
## Dense Point Cloud
![ Jonathan dense point cloud in Agisoft]({{ site.baseurl }}/images/Screenshots/densepointcloud.PNG " Jonathan dense point cloud in Agisoft ")
After cutting out anything that isn’t near Jonathan, I rendered the dense point cloud.  Once this was done (another 3 hours) I finally got to see just how impressive this software was. Without the model, or the texture, it looks amazing. I mean form pictures to that in less than 5 hours is still mind blowing to me – even a few days in.
## Model
![ Jonathan model in Agisoft]({{ site.baseurl }}/images/Screenshots/model.PNG " Jonathan model in Agisoft ")
Next I had to render the model, which took a lot less time ( a hour or two) and resulted in a nice neat model for in-game use. However it has some issues, namely the fact it is built up of 498,445 million faces. This is a crazy high number, something that I will need to lower in ZBrush so it won’t crash the engine when I start adding more than one model to a scene.
## Texturing
![ Jonathan model textured in Agisoft]({{ site.baseurl }}/images/Screenshots/textured.PNG " Jonathan model textured in Agisoft ")
Finally the texturing, which took the shortest amount of time (10 to 15 minutes), but had the biggest impact on the final result. Since the texture is created from the photos of the object, all the details that the mesh is missing is filled in with the texture itself. For Jonathan, this would be his eyes, the fur ripples and the texture of the rock itself. All these small additions makes it a stunning final result.
# Unreal and the Oculus
![ Jonathan statue in Unreal 4]({{ site.baseurl }}/images/Screenshots/Ingame.PNG " Jonathan in Unreal 4")
Bringing it into Unreal was simple enough, however it did need to be scaled up 20 times larger for some reason. I feel I will be able to fix this in ZBrush later on in the semester. On the Unreal side of things I lowered some settings as outlined by [Jack Pritz]( http://jackpritz.com/1/post/2014/09/optimizing-frame-rate-in-unreal-engine-for-the-oculus-rift.html). This helped fix _some_ issues and get the game up to a steady 70fps. However for some reason it drops down to the 40’s as time goes on. I plan to look into this and fix this in the future since this takes a heavy toll on immersion and persistence for the player.
![ Jonathan statue in Unreal 4 with Oculus]({{ site.baseurl }}/images/Screenshots/OculusView.PNG " Jonathan in Unreal 4 with Oculus")
# Next steps
I plan to try another render, this time of a different location on campus, as well as trying to get some of the background buildings in the final render as well. I hope to change out the lens for something with less of a wide angle, and I plan to clean up this new larger mesh in software in hopes of keeping the render time reasonable even though it may very well not be because of the size and scope of this render. In short, I will try and push the limits of the software, finding the breaking points of it will allow me to get a better scope of what needs to be done.
