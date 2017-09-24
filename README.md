# webos-doctor-mirror-maker


So you want your own mirror of webOS Doctor files downloaded directly from the 
'Palm' servers. The good news is that there are 54 files still available as of 
24 Sept. 2017! These are all of the files from the webos-interals list with 
active links at: http://webos-internals.org/wiki/WebOS_Doctor_Versions


## Getting Started

These instructions will get you a copy of the project up and running on your 
local machine.

### Prerequisites

These scripts rely on `wget` and they are only tested on Linux where most 
(all?) distributions include it. They might run on MacOS if `wget` has been 
installed.

The full list of webOS Doctor jar files occupy XXX GB of space, so choose a 
location with at least that amount of free space!

### Installing

CD to a spot where you want to create your mirror and clone this repo.

```
git clone https://github.com/bbito/webos-doctor-mirror-maker.git
```

## Running the scripts

Run these scripts from the terminal so you can see progress and errors.

Right-clicking a script and choosing `Execute` will run it, but you will not 
see any progress or errors and have no easy way to kill the script. **__This 
method is strongly discouraged.__**

Both scripts can produce the same results, but the script 
"make-mirror-from-palm-domains" will only work if your `/etc/hosts` file has been 
modified with:
```
195.22.200.42    downloads.help.palm.com
```

The script "make-mirror-from-palm-ips" should work whether or not the `hosts`
file has been altered.

After cloning the repo, cd into the "webos-doctor-mirror-maker" folder:

```
cd webos-doctor-mirror-maker
```

Then run your chosen script:
```
./make-mirror-from-palm-ips
```
or
```
./make-mirror-from-palm-domains
```

The chosen script will run showing progress and/or errors in the terminal.

## Authors

* **Buck Bito** - *Initial work* - [bbito on Github](https://github.com/bbito)

## Acknowledgments

* List of URLs came from webos-internals, see: http://webos-internals.org/wiki/WebOS_Doctor_Versions
* Thanks to Herrie for making me wonder how to make making a mirror easy!
