# keep-it-secure

Create encrypted records with SHA512 fingerprints, access and validate when needed.

## How to use?

All operation depends on two files:
1. `config.toml` - this is used to store the configuration. It's security is not very critical, but it's recommended to keep it safe.
2. `record_book` - this file must be kept safe, it only contains file names and checksums but needed for linking plaintext to ciphertext. It can be safely synced to any public/private backup provider.

### Creating records (`pack.py`)

```bash
./pack.py -i <input_file> -o <output_file>
```

### Verifying and decrypting records (`unpack.py`)

```bash
./unpack.py -i <input_file> -o <output_file>
```

### Updating configuration (`config.py`)

```bash
./config.py \
    [-r recipient_keyID] 
    [-h hash_vault]
```

> It's that simple!

## How it works?

View the [whitepaper][1] for more information.

## Contributing

I welcome contributions to enhance and improve this project! Whether you want to fix a bug, add a new feature, or suggest an improvement, your contributions are highly appreciated.

Just so you know, by contributing to this project, you agree to license your contributions under the same license governing this library. If you're unsure or have questions about the contribution process, please get in touch with me by opening an issue.

> (yes, I use the same text for every project I own, I'm lazy)

## Credits

Feel free to contact me for collaboration on anything!

Ferit Yiğit BALABAN, <[fyb@fybx.dev][llmail]>

[My Website][llwebsite] • [My Bento][llbento] • [X][llx] • [LinkedIn][lllinkedin]

[0]: https://www.gnupg.org/
[1]: https://github.com/fybx/keep-it-secure/blob/main/docs/keep-it-secure%20whitepaper.pdf
[llmail]: mailto:fyb@fybx.dev
[llwebsite]: https://fybx.dev
[llbento]: https://bento.me/balaban
[llx]: https://x.com/fybalaban
[lllinkedin]: https://linkedin.com/in/fybx