spongent benchmark
=================

`bench` is a programme to benchmark the cryptographic hash function spongent. It reads random input data (from 12 Byte to 16 MiB) and hashes the data 10 times. The results file contains cpu information and for each input length the runtime provided by the C-function clock(). 


Run

    $ make

to build the executable (`bench`).

Then, run

    $ bash ./RUN_BENCH.sh

to run the actual benchmarks. The results will be written to file
``RESULTS-spongent-<HOSTNAME>.txt``.V

The `bench` program uses `random.data` as source of random data. This file was created running

    $ dd if=/dev/urandom bs=1MiB of=random.data count=16

and therefore contains 16 MiB of random data from /dev/urandom.


Refercence Code
---------------

The reference code for spongent used here can be obtained from

    https://sites.google.com/site/spongenthash/downloads

Here you can find further description of the function.

