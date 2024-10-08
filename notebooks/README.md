# Notebooks for the Mitsuba study

## General Notes

Simple objects can be described directly in the XML format adopted for the Mitsuba
projeect, while more complex objects can be ingested in the OBJ format and presumably
be produced by external applications.


## Questions

* What's the coordinate system?
   * The _X_ and _Y_ appear to have the origin in the center of the box containing the scene.
   * _Z_ goes towards the viewer; placement of objects in _XYZ_ is defined in the __transform__ tag via
   its nested __translate__ tag. Negative _Z_ values correspond to moving deeper into the scene.
   * There is normalization to **1** for the coordinate numbers and sizes
   * The "scale" parameter sets the size of the object, presumably default is "1.0"

## Light sources (emitters)

In the [Geant4/Cherenkov paper](https://arxiv.org/pdf/2309.12496) the light source was formed based on a custom model and
not the _spot_ type of emitter in Mitsuba.

## Includes

There is an "include" tag which allows to include XML description of scenes in
top-level XML files. One example is in the _../scenes/colors.xml_ file, which contains
some color definitions commong across a few notebooks.
