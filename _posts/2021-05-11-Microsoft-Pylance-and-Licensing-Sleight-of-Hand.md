---
layout: post
title:  "Microsoft, Pylance, and Licensing Sleight of Hand"
date:   2021-05-11
---

[Pylance](https://github.com/microsoft/pylance-release) is a closed source tool created by Microsoft to provide various features to the VSCode editor when writing Python code.

Today, [vscode-python](https://github.com/Microsoft/vscode-python) was updated to fetch Pylance automatically and install it without prompting the user.

This means that the previously fully open-source, MIT licensed Python tool for VSCode now downloads a closed source binary in the background without mentioning to the user that the license terms have now changed.

Microsoft did in fact update the terms to include the following text:

> All the source code for the Python extension for Visual Studio Code is available under the MIT License (given below) as is the source code for the Jupyter extension for Visual Studio Code. But the optional Pylance extension for Visual Studio Code is only available in binary form and it is not licensed under the MIT License. The Pylance extension for Visual Studio Code is licensed under a Microsoft proprietary license, the terms of which are available here: https://marketplace.visualstudio.com/items/ms-python.vscode-pylance/license.

But does not warn the user that this install will occur or that the license has changed -- it just fetches Pylance without asking.

This is a user-hostile, abusive action for people who care about open source and carefully vet the tools they install and use.

There is a way to continue using the normal, fully open source Python tool, but it is no longer the default.

1. Remove the Pylance installation by clicking "Uninstall" in the Extensions side panel.
2. Edit the settings of the Python tool to set `Jedi` as the default language server.
3. Restart VSCode

This is a PSA to carefully vet your tools and turn off automatic updates if you don't want Microsoft or some other developer to casually change the license without warning. I would also suggest using [VSCodium](https://vscodium.com/), which will remove the proprietary blobs that Microsoft packages on top of VSCode as well.

This is a disappointing move by Microsoft to take a well-used and functional Python tool and inject a closed-source, properietary software binary without even the chance to consent. When licences change, users must be notified and given the chance to accept or decline the new terms, not have to catch Microsoft in a sleight of hand maneuver. 
