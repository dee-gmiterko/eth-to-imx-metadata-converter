# Ethereum to Immutable X metadata converter

Tool for converting ERC-721 metadata format into Immutable X compatible format


# Installation


    $ pip install eth-to-imx-metadata-converter


# Usage

To use it:

    $ eth2imx-meta [sorce directory] [destination directory]

Source directory:

    /eth
        1.json
        2.json
        3.json

1.json:

    {
        "name": "Bunny #1",
        "image": "https://example.com/metadata/1.png",
        "attributes": [
            {
                "trait_type": "Body",
                "value": "Fluffy"
            },
            {
                "trait_type": "Angry",
                "value": "no"
            }
        ]
    }

Convert:

    $ eth2imx-meta eth imx

Destination directory:

    /imx
        1.json
        2.json
        3.json

1.json:

    {
        "name": "Bunny #1",
        "image_url": "https://example.com/metadata/1.png",
        "Body": "Fluffy",
        "Angry": false
    }

For further options see

    $ eth2imx-meta --help
