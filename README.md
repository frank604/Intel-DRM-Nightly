### Linux Intel DRM Nightly Branch

For my Dell XPS 13 9350, I feel as though Intel is bringing quite a few patches for stability/performance/powersaving.  
Instead of waiting for them to be merged to Mainline, why not just use the Intel DRM branch?

I've added the NVME power saving patches to this.

This branch is highly recommended for those using docks and other peripherals that aren't working too well on mainline.

### Patches and Update Notes

Seems NVME power saving patch by Andy L. is already merged into Intel DRM Nightly.  No other patches applied to current pkgbuild.

Please consider using the pkbuild from AUR as this repo is only maintained when there is a necessary patch to be applied on top of the AUR pkg.

~~4.9.x has an issue with booting.  I've modified the config as discussed in bug tracker until these issues are resolved. ~~

~~4.10.x defaults to s2idle instead of deep, run:
````
sudo sh -c "echo deep > /sys/power/mem_sleep" 
````
### Recommended Install
````
git clone https://github.com/frank604/Intel-DRM-Nightly

makepkg -sfi
````

