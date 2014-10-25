# SMS77 Notification #
----------

Adds a notification per SMS via sms77.de to your check_mk.
Cheap SMS Monitoring!

## Installation & Upgrading ##

Remove existing `sms77.mkp` if exists.

    $ rm -f sms77.mkp

Then download the newest package file.
**Note:** The link below is updated on each new update.

    $ wget "https://github.com/Bubelbub/check_mk/blob/master/sms77/sms77-1.0.mkp?raw=true" -O sms77.mkp

Install the package.

    $ cmk -vP install sms77.mkp

You could delete the `sms77.mkp` if you want.

## Configuration ##

First, you must open the Check_MK webinterface.
There you click on `Users` in the `WATO · Configuration` tab.

Then you click on `Properties` at the user you want to change.

The most important thing is the `Pager address`!
Here you need to enter your mobile phone number!
Example: 004916012345678
-> Germany (0049), Telekom (160), Number (12345678)

At the `Notifications` section you should check the `enable notifications` checkbox.
After that you should have a basic configuration like `Notification time period` `Always` or something you want else.
You could check all checkboxes at the `Notification Options`, because thats not necessary for us, i think.

You must select `Flexible Custom Notifications` as the `Notification Method`.
Then you can add your SMS77 configuration.

Option | Value
------------- | -------------
Notification Plugin | SMS77
Plugin Arguments | Your username<br>Your (encrypted) [password](https://www.sms77.de/options.html?sub_opt=http)<br>Type of SMS*: basicplus, quality, festnetz, flash<br>* Optional

The other options could be the default or something you want.
For example you want only critical things per SMS.
Or you want only SMS notifications for specific hosts.

If you have questions you could ask ;)

Example pictures.
Configuration of identity: http://i.imgur.com/nKrkCHj.png
Configuration of notification: http://i.imgur.com/CX9910z.png

## License ##

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/ "Creative Commons License")

check_mk Addons by [Bubelbub](https://github.com/Bubelbub) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-a/4.0/).
