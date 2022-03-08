this is my zmk config repo. it contains zmk configs for my zmk keyboards

# TODO
- convert my layouts to all be the same layout but use custom matrix transforms to map the layout to a new board.
  this way I can make changes to the layout itself, including combos and whatnot, without having to make changes to every shield's layout, just the main layout. And onboarding a new shield is simply writing a custom matrix transform that maps the layout's expectations to the shield. Should be pretty easy. This *does* make it hard/impossible to support extraneous keys easily, like an extra thumb or extra pinky or something, but I don't have any of that just yet.
