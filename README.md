# Octave Quickstart

## Mac installation

```
brew tap homebrew/science
brew update && brew upgrade
brew install octave
```

## Ubuntu installation

If you are not on Ubuntu 16.04, you can install via apt.

```
apt install octave
```

However, if you are on 16.04, this will end up installing Octave 4.0.0, which has some problems with the exercise submission code for the Stanford Machine Learning course. In that case, you can try compiling Octave.

### Compiling Octave from source

Edit your sources.list:

```
sudo nano /etc/apt/sources.list
```

Find these lines and uncomment them:

```
# deb-src http://gb.archive.ubuntu.com/ubuntu/ xenial main restricted
# deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe
```

Now you're ready to build Octave! Warning: this will take a long time.

```
sudo apt build-dep octave   # install build dependencies
wget ftp://ftp.gnu.org/gnu/octave/octave-4.0.3.tar.gz
cd octave-*
./configure
make
sudo make install
```

## Jupyter installation

```
mkvirtualenv -p python3 jupyter
pip install jupyter octave_kernel
python -m octave_kernel.install
```

## Jupyter notebook notes

To run:

```
jupyter notebook
```

Keyboard shortcuts:

```
Shift-Enter - Run cell, select below
Ctrl-Enter - Run cell
```
