# Meta 3MF

The [3MF specification](https://3mf.io/3mf-specification/) allows putting all the data necessary for defining a 3D printable object or set of objects.

But like many broad specifications, it often is not concrete in it's definitions. Opting instead to cover the broadest possible definition for what it is defining.

In the case of 3MF, a sizable amount of the specification relates to the model geometry and data to be applied to the model geometry such as color and material.

This leaves one large area of the specification up to the user of 3MF: metadata

The primary users of 3MF are those who need to export or import model data, with no real definition of how the model data should be used. This means that common users of 3MF, primarily slicers, will define their own formats and metadata for a 3MF.

As a result, a 3MF created by [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer) does not translate to [Cura](https://github.com/Ultimaker/Cura) which does not translate to [Bambu Studio](https://github.com/bambulab/BambuStudio) and more.

## The Goal

Meta 3MF's goal is to have a simple utility that can be utilized to process a 3MF into something that can be understood by the broadest number of slicers as possible.

A 3MF created by PrusaSlicer won't work with Cura outside of model data. But run m3mf on it and Cura will understand it just fine.

An important note: slicers still only know about their own metadata. So you will need to run m3mf on PrusaSlicer output so Cura can undertsand it... but then need to run m3mf on Cura's output so PrusaSlicer will undertand it. Metadata may be lost along the way, depending on how the slicer treats data it doesn't know about.

**m3mf utility is a WIP**

## libm3mf

The heavy lifting of translating metadata is done by the libm3mf library. This can be used by other programs or slicers to do the translation between formats automatically.

**libm3mf is a WIP**

### Support

| Slicer | Layer Swap |
|--------|------------|
| Slic3r | ?? |
| PrusaSlicer | ?? |
| Cura | ?? |
| SuperSlicer | ?? |
| Bambu Studio | ?? |
| Orca Slicer | ?? |
| ideaMaker | ?? |
| Simplify3D | ?? |
| KISSlicer | ?? |
