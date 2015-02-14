## REAPexpERimentation

## Setup

```
git clone https://github.com/google/REAPER
cd REAPER
mkdir build
cd build
cmake ..
make

./reaper -i /tmp/josh.wav -f josh.f0 -a
./reaper -i /tmp/wave.wav -f wave.f0 -a
./reaper -i /tmp/wa.wav -f wa.f0 -a
```

## Plot it

```
gnuplot 

> set output 'out.png'
> set terminal png size 2000,1600 enhanced font "Helvetica,20"

> plot "wave.f0" every ::7 using ($1+2.8):3 with lines, \
       "josh.f0" every ::7 using 1:3 with lines, \
       "wa.f0"   every ::7 using ($1+2.8):3 with lines;
```

![output](/out.png?raw=true "Now I'm going to write a new WAV file!")

