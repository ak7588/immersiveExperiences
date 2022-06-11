# immersiveExperiences

Final project Google Cardboard VR

# Progress logs

## June 9th:

### Summary:
- started playing with Three.JS
- outlined basics of the first scene

### Findings:
- cardboard button can communicate with the three.js!
- camera can move like in [this](https://github.com/mrdoob/three.js/blob/master/examples/webgl_effects_anaglyph.html) anaglyph example, but we will only add it after the MVP
- dynamic change of colors like [here](https://github.com/mrdoob/three.js/blob/master/examples/webgl_framebuffer_texture.html)
- glowing effect [here](https://github.com/mrdoob/three.js/blob/master/examples/webgl_geometry_dynamic.html)
- image textures can be a custom jpg material!

```
const texture = new THREE.TextureLoader().load( 'textures/water.jpg' );
texture.wrapS = texture.wrapT = THREE.RepeatWrapping;
texture.repeat.set( 5, 5 );
material = new THREE.MeshBasicMaterial( { color: 0x0044ff, map: texture } );
mesh = new THREE.Mesh( geometry, material );
```

Amina's progress:
- explored with animation options for the 3D scene
- found stuff to implement from the initial idea/inspo for the 3D scene:

![](https://jacobrcampbell.com/assets/media/2020-soul-22-people-in-flow.jpg)

Zyad:
- ...

### To Do for next time:
- explore shadows to show scene 1, where brightness depends on the distance
- unsure of how to proceed from scene 1 to scene 2. solution: playtest and get feedback
- **concept polishing**: scene/level 1 -> you fail -> scene/level 2 -> you learn -> scene/level 3 -> you understand -> fix scene/level 2 -> fix scene/level 1 -> win?! -> final twist (if we have time) -> you realize it's a 4D world!
- cool thing about concept: progress isn't linear and you don't always have to increment. sometimes to progress you need to go back and re-do something!
- think of the specific tasks to proceed from level to level
- add event listeners for single, double, and long click on the cardboard for better interaction
- _feedback loop_ with spatial audio for negative events (mistakes/learning points) to help the user. use audio as a way of spatialization. OR the feedback can be the phone vibration or change of color.
- for level 3, add goowey texture / fancy designs ON TOP of the solid


## June 10th:
- Refined the idea implementation because Three.JS and WebXR are limited on iOS
- Now the process goes like this: 1) living on a triangle and exploring around, 2) seeing from pyramid, 3) seeing the whole 3D shape.
- The premise is to finish all levels without repeating your path. But you can only do that if you gain the whole perspective of the game! So it's essential the user fails the first two stages. The audio or visual cue will be played when the stage is failed. They will be transported to the subsequent stage when fail happens. The user has a chance to go back and "fix" their journey once they gain the whole perspective. A storytelling element appears when the game is finished to outline the importance of gaining perspective and self-improvement / taking accountability to fix mistakes of the past.
- Started the coding for scene 1

Amina:
- Refine the front-end for the immersive experience
- Worked on storytelling and design files 

Zyad:
- Work on back-end and math logic behind the game


### To Do for next time:
- Add more design files
- Push the codebase
- Actually implement designs to the codebase
- Iterate 
