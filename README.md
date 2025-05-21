# IelmenDecryptor

A batch decryption program for the files of The Coffin of Andy and Leyley (for versions 2.0.9 and lower).

It will process all encrypted `.png`, `.json`, and `.ogg` files in the directory and save them to a new folder. It will not attempt to decrypt any files that are not encrypted.

You must provide your own copy of the game.

### Usage

Place the program in the main directory that contains `game.exe` and run it from the command line. By default, the program will only check the `audio`, `data`, and `img` folders in the `www/` directory. The filenames of all encrypted files must be unchanged.

Arguments:

`inputDirectory`: Specify the input directory or file. If directory, it will traverse all folders in the directory recursively.

`outputDirectory`: Specify the output directory. You must pass both arguments at once.

Example:

```
ielmendecryptor.exe inputDirectory outputDirectory
```

### Build

To build run `cargo build --release` in the corresponding directory.

### Warning

Decrypting the game assets by using the built-in JavaScript decryption functions will leave personally identifying info inside of any files that you decrypt.

The decrypted file data from this program is completely clean. You can verify this by using a hex editor.
