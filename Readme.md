Run gibMacOS.command and select OS you want.
Run BuildmacOSInstallApp.command.

Place output file in Applications folder. 

Commands to use in Terminal for bootable USB.
Depending on which macOS you downloaded, enter one of the following commands in Terminal as instructed above. Replace MyVolume in the command with the name of your volume, if different.

If the Mac you're using to create the bootable installer is using macOS Sierra or earlier, append --applicationpath to your command, followed by the appropriate installer path, similar to what is shown in the command below for El Capitan.

Sonoma:
sudo /Applications/Install\ macOS\ Sonoma.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Ventura:
sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Monterey:
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Big Sur:
sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Catalina:
sudo /Applications/Install\ macOS\ Catalina.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Mojave:
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

High Sierra:
sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

El Capitan:
sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app


Py2/py3 script that can download macOS components direct from Apple

Can also now build Internet Recovery USB installers from Windows using [dd](http://www.chrysocome.net/dd) and [7zip](https://www.7-zip.org/download.html).

**NOTE:** As of macOS 11 (Big Sur), Apple has changed the way they distribute macOS, and internet recovery USBs can no longer be built via MakeInstall on Windows.  macOS versions through Catalina will still work though.

**NOTE 2:** As of macOS 11 (Big Sur), Apple distributes the OS via an InstallAssistant.pkg file.  `BuildmacOSInstallApp.command` is not needed to create the install application when in macOS in this case - and you can simply run `InstallAssistant.pkg`, which will place the install app in your /Applications folder on macOS.

Thanks to:

* FoxletFox for [FetchMacOS](http://www.insanelymac.com/forum/topic/326366-fetchmacos-a-tool-to-download-macos-on-non-mac-platforms/) and outlining the URL setup
* munki for his [macadmin-scripts](https://github.com/munki/macadmin-scripts)
* timsutton for [brigadier](https://github.com/timsutton/brigadier)
* wolfmannight for [manOSDownloader_rc](https://www.insanelymac.com/forum/topic/338810-create-legit-copy-of-macos-from-apple-catalog/) off which BuildmacOSInstallApp.command is based
