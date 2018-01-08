Mirror
======

This is a fork of the original MODX-Mirror by Digital Butter where development has ceased.

The Mirror plugin helps you to develop MODX websites faster. It synchronizes elements (templates, chunks, plugins and snippets) from filesystem with database and reverse.

### Installation

1. Download [transport package](https://github.com/digitalpenguin/Mirror/releases).
2. Upload archive to the `core/packages` folder of your MODX installation.
3. Use local search for the packages at the MODX Package Management page to find and install uploaded package.

### Usage

1. After installing Mirror, open the mirror plugin in the MODX manager elements tree. Click on the properties tab and create a new property set.
2. In your new property set, set the filesLocation property to a directory of your choice. The default is web_assets/ however it could be anything you like as a test you could try putting test/
3. Click on the System Events tab and you'll see the 'OnWebPageInit' event is selected. Under the Property Set column, change it from default to the name of the new property set you just made. This will ensure your settings are not overwritten during an upgrade.
4. Click Save.
5. To get mirror to work, you need to load a resource in the web context using the URL parameter '?flush'. (The parameter is also something you can change in the settings.) So if your website is www.example.com, you would load it with www.example.com?flush
6. A directory at the location you specified should have been created containing 4 subdirectories: templates, snippets, chunks and plugins. You'll find everything has been replicated from the database to the file system.
7. Now you can use your favourite IDE or text editor to develop directly with those files and you just need to load www.example.com?flush to sync your changes to the database.