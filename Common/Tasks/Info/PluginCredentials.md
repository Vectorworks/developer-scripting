## Info

Vectorworks 2026 enforces plug-in security by ensuring that all externally provided (i.e. third-party) plugins are of known origin. Vectorworks will still load and use unknown plugins, but it will show a warning dialog at launch time, letting the user know which plugins are developed by an unknown party.

This will include SDK and obfuscated Script (i.e. release version) plugins.

Currently, Vectorworks executes any plugin placed in the Plug-ins folder, which means that Vectorworks is running code within the Vectorworks environment that might be of unknown origin and thus reduces the security of the entire application.

__Here’s what you need to know as a user:__
* Vectorworks 2026 will require a ‘Credentials’ file for each developer containing all plugins from this developer.
* Script plugins that are not locked \[open-source plugins] will not be required to have Credentials. This means that custom user plugins will not be considered security risk.
* Vectorworks will provide a way to see all developers of the currently loaded plugins, and all the features each plugin provides.
* Vectorworks will issue Credentials files to all our partners that develop plugins.
* The Credentials file will contain information about the developer. It will not be bound to the bytes of the plugin, but it will be cryptographically signed and validated.
* The signature validation will not require online access. It will be performed via a “public key” validation.
* The user will still be able to use plugins from Unknown developers, after manually enabling them, for the user to not lose features.
* Vectorworks will warn the user if a plugin is not “signed” at launch time and by default it will disable them.
* The user can manually enable unknown developer plugins but still be warned of the potential risks at every launch of Vectorworks.

__For the developer:__
* Every SDK and encrypted/obfuscated Script \[VectorScript and Python] plugin needs a credentials \[binary] file.
* One developer requires only one credentials file that will cover all their plugins.
* The developer must fill out a .json file (see the details below):
  * Containing name, email for the developer.
  * Containing a list of plugins, listing file names without extension.
  * The .json file must be submitted to Vectorworks to generate the credentials binary-file, and it will be provided back as part of the Vectorworks Partner program.

    Please email the .json file confirming security key request to: [developer@vectorworks.net](mailto:developer@vectorworks.net)

  * The credentials file has .vst extension and Vectorworks will not confuse it with a script tool.
  * The credentials file must be distributed alongside (same folder) of the plugins it covers. The presence of all plugins it covers is not necessary, this  means that you can use the same credentials file for partial plugin distributions.
  * A new credentials file will be needed for each version after Vectorworks 2026.


## Developer details

__For the developer: credentials file details__

The credentials file is an encrypted version of a .json file that defines the developer, 
with the following format:
```json
{
  "developer": {
    "name":"my-company-name",
    "contact": "support@developer.com",
    "website": "https://www.my-company-name.com",
    "issueDate": "2025-09-10"
  },
  "files":[
    "file-name-no-extension",
    "another-file-name-no-extension"
  ]
}
```

This file lists “developer” information: name, contact email, and date of issue. It also defines a list of file names \[without extension] of all plugin files (SDK or script) covered by this credentials file. There is no limit to how many plugins can be included in a credential file.

