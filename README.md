Vim
===

I use Vim on Windows. Call me crazy, but I like it.

Installation
------------

Although I am a fan of [Chocolatey](https://chocolatey.org/) I choose to
install Vim using the official installer, not by the Chocolatey package.

*	Download the latest Windows installer from the Vim website.
*	Launch the installer and follow the wizard steps. I prefer to install Vim in
	my `C:\Tools\Vim` folder.

Additional Tools
----------------

*	Python 2
*	Exuberant Ctags (`choco install ctags`)
*	Ack! (`choco install ack`)

Configuration
-------------

* 	Navigate to the Vim installation folder.
* 	Delete the `autoload` folder from the `vim74` folder.
* 	Delete the entire `vimfiles` folder.
* 	Checkout this repository to replace the `vimfiles` folder, make sure to include the
 	submodules: `git clone --recursive https://github.com/jnsn/vimfiles.git`.
* 	Remove the `_vimrc` and create a hard link to the `vimrc` file in the
	`vimfiles` folder. On Windows this can be done with the following command:
	`mklink /H _vimrc vimfiles\vimrc`.

### Optional

As seen from the configuration above, I create my backup and swap folder in
the runtime folder.  This is a personal preference. Remove the lines from the
`_vimrc` file if you don't want them, otherwise create the required folders in
the `vim74` folder: `tmp/`, `tmp/backup/` and `tmp/swp/`.


