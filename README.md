# Surfed Localization

This is the community language repository for [Surfed](https://surfed.app).

If there is a language you'd like to see Surfed localized to but we haven't got around to it yet, and you have some git-fu, feel free to submit a pull request to the repository.

Please do not add multiple languages in the same pull request — this way, there can be a discussion thread for each language for any changes or tweaks that need to be made, and give others opportunity for peer review.

The latest translation files are available in the branch `development`. Please switch to this branch and edit or add your localization from this branch.

## Folder Structure
Languages are structured in folders as such:

`en.lproj/Localizable.strings`

Where `en` is replaced by the [ISO 639-1 two-letter language code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), and the `Localizable.strings` file is structured as per the English (`en`) version.

Please do not include any other files in a pull request.

### Files and Subfolders

Every language folder contains the following files:

####  Localizable.strings

This is file contains the strings of the app and app extensions. 
It would be great if this file could be translated completely.

####  InfoPlist.strings

This is file contains the strings of the app shortcuts. 
It would be great if this file could be translated completely.

####  Action Extension/ InfoPlist.strings

This is file contains the string of the action extension name. 
It would be great if this file could be translated completely.

####  Safari Extension/messages.json

This is file contains the strings of the Safari extension popup. 
It would be great if this file could be translated completely.

####  In-App Help/support.json

This is file contains the strings of the in-app help. 
This file is very extensive and does not necessarily need to be translated. Nevertheless, I would be very pleased.

## Localization

Strings are denoted as `"KEY"` = `"value"`, where the keys remain the same across all languages, and the values are localized. There must be a `;` at the end of each line.

`"SEARCH_KEY" = "Search";`

Where you see a `%@` or `%ld` token, this denotes a value that is replaced at runtime — in most cases will be the user-provided name for a station or collection, or a number. The corresponding localized value must keep the token in the right place to provide the same meaning as the English value.

`"IMPORT_TITLE" = "Import \"%@\"?";`

`"IMPORT_BODY" = "This shared collection contains %ld stations.";`

## Translate with AI Prompt (experimental)

The French localisation was translated experimentally with the help of OpenAI. To get a better result, the AI prompt was created with context to the app and an instruction on what the structure looks like and which placeholders to keep or characters to escape.

The following prompt was used for the `*.strings` files:

```
Localise the following key/value entries into French. Context: The strings belongs to the iOS app Surfed, which is a history and bookmark manager and web automation tool. The left value is the key and the right value after the equal character is the the value. Key and values are wrapped inside double quotes. The left key should not be translated. Please keep placeholder characters like %@ or %ld, which will be used for dynamic values. Double quotes inside the key and value needs to be escaped by a slash. Every line needs a semicolon at the end:
```


The following prompt was used for the `*.json` files:

```
Localise the following JSON entries into French. Context: The strings belongs to the iOS app Surfed, which is a history and bookmark manager and web automation tool. The left value is the key and the right value after the colon character is the the value. Values are wrapped inside double quotes. The key should not be translated. Double quotes inside the value needs to be escaped by a slash:
```

## Credits

Please append the name you would like to be credited by to the pull request or the comment block at the top of the Localizable.strings file.

## Source

This project has been inspired by Steven Troughton-Smith and the community language support for the app [Broadcast](https://github.com/steventroughtonsmith/broadcasts-localization)
