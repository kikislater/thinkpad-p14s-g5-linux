<p align="center">
    <img src="images/thonkpad.gif" />
</p>

# ThinkPad P14s Gen 5 — Linux

Various configs for Lenovo ThinkPad P14s Gen 5 running under GNU/Linux distributions.

## General

Reading the [Arch Wiki article](https://wiki.archlinux.org/title/Lenovo_ThinkPad_P14s_(AMD)_Gen_5) about the laptop is highly recommended, even if you are using another distribution.

## Sound

The default speaker sound is terrible, so the repository includes [EasyEffects](https://github.com/wwmm/easyeffects) presets to make it better. This includes:
* Dynamic, Game, Movie, Music, and Voice presets using convolver effect config taken from P14s G5 Windows installation ("ThinkPad P14s G5 - Dynamic", "ThinkPad P14s G5 - Game", "ThinkPad P14s G5 - Movie", "ThinkPad P14s G5 - Music", "ThinkPad P14s G5 - Voice")
* A mix of a modified LoudnessEqualizer preset from [Digitalone1/EasyEffects-Presets](https://github.com/Digitalone1/EasyEffects-Presets) and a Music/Movies convolver effect config taken from T14s G3 Windows installation ("ThinkPad P14s G5 - Legacy" preset)

To install the presets, just run the following command:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/kikislater/thinkpad-p14s-g5-linux/master/install_easyeffects.sh)"
```

Then, to use it, open EasyEffects, and select one of the "ThinkPad P14s G5" presets in the "Presets" menu in the upper-left corner of the application window.

## Fan control

To make the fans run quieter, [thinkfan](https://github.com/vmatare/thinkfan) can be used. See [this article](https://blog.monosoul.dev/2021/10/17/how-to-control-thinkpad-p14s-fan-speed-in-linux/) to learn how to configure it - but use this repository's [thinkfan.conf](https://raw.githubusercontent.com/m4tx/thinkpad-p14s-g4-linux/master/thinkfan.conf) file instead. Note that the config assumes you have the AMD version of the laptop (but should be easy enough to modify for the Intel edition, too). Note that increasing the system temperatures might result in shortening the lifespan of the laptop, so use with caution.

## Attribution

The EasyEffects convolver configs are taken from [qwreey](https://github.com/qwreey/thinkpad-t14-gen5-amd-impulses).
