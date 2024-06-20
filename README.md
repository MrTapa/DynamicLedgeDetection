# DynamicLedgeDetection for the Motion Matching Sample provided by Epic:
https://www.unrealengine.com/marketplace/en-US/product/game-animation-sample

A detailed breakdown of how this component works under the hood is present here:
https://x.com/MrTapa/status/1803587612650635421

Extract the two uassets in `/GameAnimationSample/Content/Blueprints` of the sample project.
Add the component to the character blueprint found in: `/GameAnimationSample/Content/Blueprints/CBP_SandboxCharacter`
Inside the `Try Traversal Action` function of the character, replace the node inside the step labled `2.2` with a the function `Try and Calculate Ledges`
Now you can remove the assumption about traversable block actors, so right before step 2.2 you can remove the cast to that specific type
Traversal actions should now work for all geometry that `looks traversable`

This has been tested on the sample project for UE 5.4.2
