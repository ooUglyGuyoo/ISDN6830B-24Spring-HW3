# ISDN6830B-24Spring-HW3

## Demo Video
https://photos.app.goo.gl/LvdRHtqo39M6JkNZ7

## Environment setup
The server.py is running on my PC through anaconda with python, opencv and yolov8 installed. The phone is connected to the same network as the PC. The HW3.cs is running on unity (on phone).

## Code explaination
The process of the project is as follows:
1. The photo is captured and send to the server.py which is running on my PC.
2. The server.py will process the image and feed it through the trained model (best.pt).
3. The model will return the center of the bounding box (bikes or human) in the image.
4. The point coordinate is sent back to the phone which is running the HW3.cs on unity.
5. The point is normalized and raycasted to the 3d world to find a 3d coordinate.
6. An object (a capsule) is created at the 3d coordinate.

The corresponding code can be found in  and HW3.cs.

## Problems
1. There is a small object created at first when I start the program. I don't really have time to figure out why. But it is not a big problem.
2. The model is still the model submitted in HW2. It is not trained on the new dataset. The model is not very accurate but it is good enough for the purpose of this project.
3. As you can see the in the demo video, the 3d point of the created object is not correct. The object is created in the wrong position. I cannot really figure out why since if I use the pixel coordinate of the image, the object won't even be created (nothing is hitted).

Thanks Sean for giving me good guidance at the start btw, or it will take me a lot of time to figure out how to make the template work lol.