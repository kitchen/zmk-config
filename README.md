this is my zmk config repo. it contains zmk configs for my zmk keyboards

# philosophy
I daily a 34 key keyboard. It has plenty enough keys for me, for most things. But I also own a bunch of keyboards, and would like to make sure they all have current firmware that matches my layout and whatnot. Some of them are more than 34 keys, so I can't just use *one* layout for them all.

Except, I can!

I have [one standard layout](config/standard-keymap.dtsi) that I use. It has all of my combos, all of my modtaps and whatever other relevant configs.

I then use custom matrix transformations to apply them to keyboards. Examples: [kyria](config/kyria.keymap), [reviung41](config/reviung41.keymap). This way, when I update my keymap, I only have to update one place, and numbering for things like combos remains consistent. Any keys that are not part of my standard 34 key keymap are simply left unconfigured.

I do have a few "extra keys" in my standard keymap that I can bring in in custom matrix transform, but they are optional and if the keyboard doesn't have enough keys, they just don't get mapped to anything.

Why even have keyboards that have keys that I don't use? I like building keyboards, and I collect them. I doubly like it when they actually function :)

I also am a [dvorak layout](https://en.wikipedia.org/wiki/Dvorak_keyboard_layout) user, and I have a very difficult time keeping track of what dvorak key maps to qwerty in my head, so I created a [header file](config/dvorak-defines.h) that has a list of defines so I can put, e.g. `DV_H` in my keymap files and it'll spit out the correct qwerty code. Oh, and I map the keyboard to dvorak in software on the host side, not on the keyboard side. This is primarily because I am a laptop user and I want to be able to use the laptop's built in keyboard, and doing this means I don't have to constantly change the keymap around on the host when switching between custom external keyboard and built-in laptop keyboard. Also it means I can use *any* standard keyboard with my computer directly without switching the layout, as I do sometimes for gaming with my Apple Magic Keyboard.


# License
To the extent anything in this repo even *can* be licensed (it's mostly just config files, after all), I apply the [WTFPL](http://www.wtfpl.net) license. Note that there may be some stuff in here I copy/pasted from elsewhere which might be licensed differently, so do your research or whatever. I try to put license/copyright info in the files directly where applicable.

