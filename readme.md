# hdf5-dna

Examples and experiments of using HDF5 and h5py with biological sequence data.

## Features

- Create HDF5 database from any sequence format that BioPython supports
  (FASTA, FASTQ, ...)
- Output sequences from HDF5 database
- Randomly sample sequences from HDF5 database

see `bin/*` for details.

## Tests

Just run `test/test-hdf5-dna`.

### Pre-Commit Hook

Add this to `.git/hooks/pre-commit` to run the tests before committing.

```sh
test/test-hdf5-dna 2>/dev/null

if [ $? -eq 0 ]; then
  echo "Tests passed."
else
  echo "Tests failed. Aborting commit."
  exit -1
fi
```

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
