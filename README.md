AE2Blend V1.1 will soon be available on the Blender Market.

Camera Tracking Demo: https://www.youtube.com/watch?v=zzGa4rD46CQ

#AE2Blend V1.0

AE2Blend is an addon for Blender 2.7x that lets users copy keyframe and transform data from Adobe After Effects, and apply it directly to new or preexisting objects in Blender.

#How to use

Once AE2Blend.py is downloaded, installed and enabled, the panel can be found in the Animation tab in Blender's 3D View.

Inside After Effects the user selects one or more transform channels (position, scale, rotation and orientation), and copies them to the clipboard by holding control or command and pressing "c", or Edit > Copy.

Then using the AE2Blend panel the user simply pastes the transform data to a selected object using the "Paste Keyframes" button, or uses one of the "Create..." buttons to create a new object with the transform data.

#Settings

[Scale]

The value position and scale keyframes are divided by. The coordinate system in After Effects is based on pixels, so values can often be in the hundreds to thousands. A higher Scale value creates smaller position and scale values.

100 is default because most position values will be placed within Blender's default view, and a 100% scale in After Effects will translate to 1.0 scale in Blender.

[Delta Rotation]

After Effects provides two sets of rotation values for each 3D object; individual xyz angles and orientation. This setting lets the user determine which of these values is assigned to the object's delta rotation in Blender (if either is selected to begin with).

[Starting Position]

Because the coordinate system in After Effects uses the top left corner of the screen as the origin point, all position values are inverted. This means most objects will be placed beneath the groundplane. If the user wants they can have objects in Blender begin their animation from wherever the 3D Cursor is placed. However multiple objects from the same After Effects composition will be placed relative to eachother.

[Starting Frame]

Choose whether to match all keyframes with their corresponding frames in After Effects, or to treat Blender's playhead as the zero frame.

[Create Empty]

Creates a new empty object with all of the After Effects keyframe data applied.

[Create Plane]

Creates a new plane mesh with the same porportional width and height as the After Effects object. The plane is parented to an empty object which has the keyframe data applied.

This is ideal for rectangular solids created in After Effects. Other objects may cause unexpected results.

[Create Camera]

Creates a new camera object parented to an empty object which has the keyframe data applied. The camera field of view must be manually entered. The horizontal field of view of a camera in After Effects can be found in the timeline by opening the Camera Settings attributes.

[Paste Keyframes]

Pastes all After Effects keyframe data to all currently selected objects in Blender.

#Tips and Tricks

Users may select as many or as few transform channels from After Effects as they want. AE2Blend will only apply whichever transforms are copied from After Effects.

Both 2D and 3D data can be imported into Blender. 2D data will simply remain flat along Blender's Y axis.

Static transform values (animation channels without any keyframes) can also be copied into Blender. The new or existing object will simply be set to that position, scale or rotation, with no keyframes set.

After Effects does not provide animation curve or interpolation data. Curves and interpolation must be manually set in Blender, or baked down in After Effects.

A cheat to "baking down" keyframes in After Effects is to use the Wiggler tool. Select each channel individually, set the Wiggler's frequency to your composition's frame rate (remember to add decimals with frame rates such as 23.976), set the magnitude to zero and press apply. When copied into Blender all of the curves and interpolation will be preserved, albiet much harder to edit.
