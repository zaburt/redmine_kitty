# Kitty

A light Redmine theme — a crisp white/light-grey canvas
with bold, saturated cyan, magenta, purple, orange and green accents.

## Installation

1. Clone this theme ([https://github.com/zaburt/redmine_kitty](https://github.com/zaburt/redmine_kitty)) into the Redmine `themes/`
   directory at the application root (Redmine 7+) as `kitty`:

   ```
   git clone https://github.com/zaburt/redmine_kitty.git themes/kitty
   ```

   The result should contain:

   ```
   themes/kitty/stylesheets/application.css
   ```

   > Note: Redmine 6 and earlier used `public/themes/` instead of `themes/`.

2. Restart Redmine so the new theme appears in the list of available themes.
   In production, precompile assets so the theme CSS/images are served:

   ```
   RAILS_ENV=production bin/rails assets:precompile
   ```

3. Go to `Administration -> Settings -> Display` and select "Kitty" in the
   "Theme" drop-down list. Save your settings.

Redmine should now be displayed using the `kitty` theme.

## Customize

1. You can change `images/logo.svg` to update the header/login logo, and
   `favicon/favicon.svg` to update the browser tab icon.
2. If you don't want to use a logo in the header, you can remove the
   `#header > h1` styles in `stylesheets/application.css`.
3. The palette is defined inline as hex values throughout
   `stylesheets/application.css`:

   | Role               | Color     |
   |--------------------|-----------|
   | Page background    | `#FFFFFF` |
   | Panel / box bg     | `#F3F3F8` |
   | Text               | `#201A38` |
   | Muted text         | `#6B4FA0` |
   | Primary accent     | `#00F0FF` (cyan, darkened to `#0089A8` for text) |
   | Secondary accent   | `#FF2BD6` (magenta, darkened to `#C21BA3` for text) |
   | Tertiary accent    | `#B967FF` (purple, darkened to `#7A3FD1` for text) |
   | Success            | `#39FF8F` (darkened to `#1C9A57` for text) |
   | Error              | `#FF3366` (darkened to `#D1294F` for text) |
   | Warning            | `#FFE066` (darkened to `#8A6D00` for text) |

   Bright neon hues are kept at full saturation for borders, badges,
   buttons and the rainbow menu underlines/gradients; they're only
   darkened when used as body text, to stay readable on a light
   background.

4. In production, re-run `assets:precompile` after editing any theme file.

## License

Licensed under [GNU GPLv2](LICENSE).

Copyright (c) 2026 Onur Küçük (onur [at] delipenguen.net)
