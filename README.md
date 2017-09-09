# superlumic-google-fonts

Ansible role to install a user-defined selection of Google Fonts on the computer. This role is part of the FlyingBinary extensions to the Superlumic project that aims to simplify repeat computer setups on macOS, 10.10 and up.

## Requirements

* OSX 10.10 or 10.11 or
* macOS 10.12 and above

Verified compatible at least to macOS 10.13 (High Sierra)

## Dependencies

* [IanTaylorFB.superlumic-homebrew](https://github.com/FlyingBinary/ansible-role-homebrew)

**_Note:_** You can also use the original, Superlumic, homebrew role, just change the dependency in `meta/main.yml`

## Usage

Check [Superlumic](https://github.com/superlumic/superlumic) for documentation on general use of the Superlumic project.

This role supports the global - group - personal hierarchy in Superlumic, allowing you to specify fonts to be installed for everyone, a specific group or personally. Specify global fonts in a global profile within Superlumic; group and
personal fonts in the appropriate profiles

Fonts must be correctly capitalised. Fonts with spaces in the name
must be quoted. Font names are **_not_** validated, and will fail silently.
Examples:

```yaml
global_google_fonts:
  - "Open Sans"
  - Raleway
  - Ubuntu
group_google_fonts: []
personal_google_fonts:
  - "Indie Flower"
  - "Libre Barcode 128"

```

See the Google Fonts site (https://fonts.google.com) for details of the available fonts, and more information on font usage.

The role does nothing unless at least one of these contains at least one font name at run time. All styles in the font family are installed: the installer `--variants` option is not currently supported in this role. Fonts are installed to `~/Library/Fonts`.

See the [Google Fonts](https://fonts.google.com) site for details of the available fonts, and more information on font usage.

The Google Font Installer has more functions. See the github [repo](https://github.com/lordgiotto/google-font-installer) for full details.

## License

MIT

## Author

[Ian Taylor](mailto:ian.taylor@flyingbinary.com) - [@IanTaylorFB](https://twitter.com/IanTaylorFB)
