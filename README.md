PyGRDECL: A Python-based GRDECL Visulization Library
==============================================================================================
Bin Wang (binwang.0213@gmail.com), Yin Feng
Department of Petroleum Engineering, Univeristy of Louisiana at Lafayette, Lafayette, US, 70506

<p align="center">
  <img src = "https://github.com/BinWang0213/PyGRDECL/blob/master/img/GridPreview.png" height="300">
</p>

`PyGRDECL` is a light-weight open source library for converting a Eclipse grid with properties to a vtu-file.
(to be opened in ParaView for example). 

## Install & Usage

`Anaconda 5.3` (https://www.anaconda.com/download/) and `Shapely 1.5` (https://anaconda.org/scitools/shapely) is required. The library works on both Windows and Linux.

After downloading and unzipping the current <a href="https://github.com/BinWang0213/PyGRDECL/archive/master.zip">repository</a>, navigate to the library directory and run a simple example contained in `Example_GettingStart.ipynb`:

## Getting Start

<p align="center">
  <img src = "https://github.com/BinWang0213/PyGRDECL/blob/master/img/DomeModel.png" height="300">
</p>

```python
from GRDECL2VTK import * 

#Read GRDECL File
Model=GeologyModel(filename='./ExampleData/dome.grdecl')

#Convert ECLIPSE grdecl format into VTK
Model.GRDECL2VTK()

#Decompose the model into sub-volumes in terms of faults automatically (this function requires shapely library)
Model.decomposeModel()

#Output to VTK format
Model.Write2VTU()
```


# License

This code is released under the terms of the BSD license, and thus free for commercial and research use. Feel free to use the code into your own project with a PROPER REFERENCE.  
