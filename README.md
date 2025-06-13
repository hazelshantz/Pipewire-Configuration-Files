# Pipewire audio dotfiles configuration files

This small repo contains configuration files that will improve your audio experience on Linux by setting the right values. the effects of it will be more noticeable when recording audio with pipewire-jack.
The configuration files are distro-agnostic, so they should work regardless the distro.

# Update: this repo is going archived, due to major breakage issues produced by the files. please use vanilla PipeWire config + Cable app https://github.com/magillos/Cable to manage your config!!

# About:
By default, Pipewire may not have the right settings for your audio devices, producing crackling/poppling or just giving you bad audio quality when recording, when compared to Windows. By replacing your vanilla Pipewire files with the ones on this repo, it will/should fix this on your system.

## How to?

### Requirements
- Your system must have Pipewire installed, with all it's dependencies `(pipewire-alsa, pipewire-pulse, pipewire-jack, pipewire, wireplumber, pipewire-v4l2)`
- The name of the packages (if not installed) may depend on the distro you're using, but most main Linux distros nowadays ship with pipewire, or offer it as main audio solution.
- You must have superuser permissions to manage system files (being able to sudo or doas on your system)

### Procedure:

- `git clone` this repo, or download it as zip. 
- Browse to `/etc/pipewire` and make a backup of `client.conf`, `pipewire.conf`, `pipewire-pulse.conf` and `jack.conf`, by creating a new folder called `backup` or by renaming them to eg, `jack.conf.old`
- Elevate yourself with sudo, and by using a GUI file manager, copy the files into `/etc/pipewire`, or use `sudo cp pipewire.conf jack.conf client.conf pipewire-pulse.conf /etc/pipewire`
- Once done, reboot your system and record with pipewire-jack, or play some music. you should notice an improvement.



## Tip: Install easy effects or JamesDSP4Linux to improve the audio even more.
If you want even more from your audio, either for recording or listening, you can refer to the following projects:
Note: easyeffects may suit you more, if you want a more professional way of recording audio, due to it's compressor and convolver features.
- JamesDSP4Linux: https://github.com/Audio4Linux/JDSP4Linux
- EasyEffects: https://github.com/wwmm/easyeffects

### For further audio improvements, I highly recommend you to read this repository:

https://github.com/scottericpetersen/pro-audio-on-linux

### Important note:

the configuration files provided here, have only been tested under Arch Linux. I would love feedback on other distros.



### Aknowledgements:

[@kthread0](https://github.com/kthread0) for helping me with improving my own audio, as I was having issues while recording my guitar under Arch Linux. they are the ones who made these files. I owe them a lot. so if you can, go check their repo and projects. I only take the credit of writing proper documentation for the files.
