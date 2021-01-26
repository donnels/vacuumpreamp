# vacuumpreamp
housing a retro vacuum tube china preamp

# Introduction
Have a nice wooden box that is looking for some use as a housing
The pre-amp is a cheap vaccum tube type sourced from aliexpress
https://a.aliexpress.com/_B0MVMZ

## Openscad
I've created an openscad model of the Box based on some measurments with a calliper.
The model is designed to help asses where to drill holes and to print a guide to drill the holes.
The preamp has a power input (12v~) an in and an output (headphone jack) and a Volume potentiometer.
Also the housing is to expose the Vacuum Tubes to the interested viewer.
Since the lid is hinged and the relative position of the tubes to the lid, when opening, is difficult to eyeball the model was created to try out different Hole placments as well as providing a template for Drill guides.

# Dockerizing
## Pack Openscad into a docker
```
docker build -t donnels/openscad:1.0 .
```
## Run the docker to make a testfile
```
docker run --rm --name "openscad" --volume $PWD:/data donnels/openscad:1.0 openscad -o /data/test.png /data/*scad
```
### image output
![](test.png)
