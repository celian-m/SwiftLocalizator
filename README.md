# SwiftLocalizator
Localizator helps you to manage translation in your mobile apps


## Requirements

To use the Localizator, you must be running Mac OS X, and having swift installed.

```sh
$swift -v
Apple Swift version 3.1

```

##Download

Download the latest Localizator Release `here`

## Usage

###Run
`$./Localizator localizator.plist`

###Configuration

The localizator is managed by a `.plist` file.

You can download `here` a sample of the `localizator.plist` file.



| key | type | mandatory | value |
|-----|------|-----------|-------|
|   accounts  |  [String]    |   true        |    List of account to use for authentication   |
|  fileId   |    String  |     true     |    Id of your Google Drive file   |
|  platform   |    String  |    true      |   Choose your platform ( ios \| android )    |
|   path  |   String   |     true      |   Path for your files generation    |
|  skipRows   |   Int   |    true       |    Number of row to skip ( may be your table headers )   |
|    keyColumn |   Int   |   true        |  Index of the column containing the keys     |
| commentColumn | Int | true | Index for comments. They will be inserted into the generated files. use `-1` to exclude comments |
| locales | [ { String : Any }]  | true | Array of object describing your drive file. See plist sample |




