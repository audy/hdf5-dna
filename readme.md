# hdf5-dna

Examples and experiments of using HDF5 and h5py with biological sequence data.

## Features

- Create HDF5 database from any sequence format that BioPython supports
  (FASTA, FASTQ, ...)
- Output sequences from HDF5 database
- Randomly sample sequences from HDF5 database

see `bin/*` for details.

## Parallel

This branch was created to see if h5py-mpi would work with MPI but it
turned out that you can't use h5py-mpi with vlen datasets. Since I'm not
making the assumption that your sequences will all be the same length,
we can't use mpi for h5py. However, in some cases, read lengths are
always the same (for example, Illumina). Therefore, this branch might be
useful.

## Installation

`pip install -r requirements.txt`

## LICENSE

The MIT License (MIT)

Copyright (c) 2014 Austin G. Davis-Richardson

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
