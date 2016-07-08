These files are required in order to get hfpd to run without X, on Raspbian.

/etc/dbus-1
Allow root to own the correct dbus domain on the system bus.

/etc/bluetooth/main.conf
Modifies device class of adapter to support hands free profile.

/etc/sudoers
Allow user 'pi' to run hciconfig and rfkill without entering password.

/usr/lib/systemd/system/bluetooth.service
Start bluetoothd in compatibility mode to enable sdp browse local.

dbus-headless.sh
By 'sourcing' this prior to running hfpd, hfpd will attempt to
publish services on the system bus (rather than a session bus,
which generally requires X).

