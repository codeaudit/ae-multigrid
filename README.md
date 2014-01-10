Multigrid Angular Embedding Eigensolver
---------------------------------------

This software implements the multigrid eigensolver described in:

> [Progressive Multigrid Eigensolvers for Multiscale Spectral Segmentation]
> (http://vision.caltech.edu/~mmaire/papers/pdf/seg_multigrid_iccv2013.pdf)  
> Michael Maire and Stella X. Yu  
> International Conference on Computer Vision (ICCV), 2013  

Demo
----

Run `demo.m` from MATLAB for a multiscale image segmentation demo.

Notes
-----

The current implementation is efficient for image sizes (length and width)
divisible by 2^(s-1), where s is the number of pyramid levels.  See the
included `multiscale_resize.m` function for padding arbitrary images to the
nearest efficient size.

Citation
--------

If you make use of this software, please cite the following in any publications:

    @inproceedings{MY:ICCV:2013,
        title     = {Progressive Multigrid Eigensolvers for Multiscale Spectral Segmentation},
        author    = {Michael Maire and Stella X. Yu},
        booktitle = {International Conference on Computer Vision (ICCV)},
        year      = {2013}
    }

License
-------

Copyright (C) 2013-2014 Michael Maire <mmaire@gmail.com>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

External Dependencies
---------------------

The image segmentation demo relies on local contour cues computing using the
Berkeley contour detector (Pb).  A version of this software is included in the
`grouping/` subdirectory.  For more information see:

http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html
