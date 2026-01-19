# Alarm Manager


### Purpose:
* To fix some of the papercuts that come with using GNOME Clocks on a mobile phone running Phosh.


### Done:
* Dismiss alarms early
* Play alarm even if phone is in silent, volume is down/off, or otherwise muted
* Pause media players at alarm time and resume afterwards (resume is a bit unreliable atm)
* Optionally switch to speaker output for alarm and restore state afterwards
* Optionally ramp volume up from set minimum to set maximum for gentle wake up


### To Do:
* More testing - you should consider this a warning!
* Does this even work on devices besides the FLX1s?  Who knows!?
* List dependencies (I don't remember installing anything outside of the FuriOS defaults for this)
* Change the way the interval variable is used to be more intuitive and friendly
* Make resuming of media players reliable
* Allow selection of alarm tone (maybe... I've got an idea but no clue if it would work)
* Make a less manual installation method
* Make a settings app and .desktop file for settings changes instead of editing text files


### How to install:
* Move the contents of dot-local_bin to ~/.local/bin
* Edit the contents of dot-config_systemd_user to your liking and move them to ~/.config/systemd/user/
* [Eventually] Move the contents of dot-local_share_applications to ~/.local/share/applications
* Run: ```systemctl --user enable --now alarm-volume.service alarm-dismissal.service```


### How to uninstall
* Remove the files you added to the directories above
* Run: ```systemctl --user disable --now alarm-volume.service alarm-dismissal.service```


### Shout out
* FuriLabs for making the FLX1s, the first mobile Linux phone I've ever been able to comfortably (enjoyably even!) daily drive.
* Alaraajavamma (Aki) inspired me with their [alarmvol script](https://gitlab.com/Alaraajavamma/fastflx1/-/blob/flx1s/scripts/alarmvol?ref_type=heads)


### License
* For now, this project adopts Alaraajavamma's "Feel free to do what ever you want with this but no guarantees - this will probably explode your phone xD" license
* but I reserve the sole right to change it at any point for any reason and without any notice.
