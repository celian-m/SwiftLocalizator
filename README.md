# SwiftLocalizator
Localizator helps you to manage translation in your mobile apps


## Requirements

To use the Localizator, you must be running Mac OS X, and having swift installed.

```sh
$swift -v
Apple Swift version 3.1

```

## Download

Download the latest Localizator Release [here](https://github.com/celian-m/SwiftLocalizator/blob/master/bin/Localizator)

## Usage

### Configuration

The localizator is managed by a `.plist` file.

You can download [here](https://github.com/celian-m/SwiftLocalizator/blob/master/localizator.plist) a sample of the `localizator.plist` file.



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

#### Locale Object
The locale object used in the `locales` key should looks like :

```xml
		<dict>
			<key>overrideColumn</key> <!-- optionnal -->
			<integer>2</integer> <!-- Provide a fallback column -->
			<key>subpath</key>  
			<string>values</string> <!-- Will be appended to {path} -->
			<key>column</key>  <!-- The column index  -->
			<integer>3</integer>
		</dict>
```
### Run
`$./Localizator localizator.plist`

### Tip

#### Webloc
Use `$./Localizator localizator.plist -w` to generate a shortcut to your drive file

#### Shortcut

- Copy the `Localizator` binary into  `/Library/Localizator/Localizator`
- Export the new PATH as `$export PATH=$PATH:/Library/Localizator` ( could be pasted in `~/.bash_profile` )
- Run `$Localizator` from anywhere



