# Installing programs

## Lammps fast install

```bash
git clone -b release https://github.com/lammps/lammps

cd lammps && mkdir build && cd build
cmake ../cmake
cmake --build .

cd ../src
make yes-manybody
make serial

../lammps/src/lmp_serial -in in.graphene
```


## VMD install
```bash
load https://www.ks.uiuc.edu/Development/Download/download.cgi?PackageName=VMD

cd vmd
./configure

cd src
make install

>> vmd
```

## SPGLIB
https://spglib.github.io/spglib/install.html
```bash
git clone https://github.com/spglib/spglib.git

tar xvfz 
cd spglib

mkdir _build && cd _build
cmake -DCMAKE_INSTALL_PREFIX="" ..
make
make install
```

## FFTW
http://www.fftw.org/fftw3_doc/Installation-on-Unix.html
```bash
load http://www.fftw.org/download.html

./configure
make
make install
```

## FixPhonon
```bash
load https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/fix-phonon/FixPhonon-1.75-all.tar.gz

mv ./USER_PHONON ./lammps/src/
sh Install.sh 1

make yes-user-phonon

```

## Latgen
```bash
git clone https://github.com/lingtikong/latgen

```
