# Time Zone Builder

### _Dynamically generate Posix Time Zone String using pure JS and browser functions_

Use case would be an IOT project where you use NTP to sync time and you need to set the right Posix time zone string for the correct local Standard/Daylight Saving time. When using an app from the browser to control the device, you can get the Posix time string and upload it to your device. The Posix Time Zone string is constructed using standard JS browser functions.

It will not use region specific Time Zone codes like CET, CEST, EST, EDT etc. In stead it uses general UTC notation (which is valid). The codes are only used for display in certain formats. The most important parts are the offset for STD time and DST time plus the DST rule. When using the generated Posix string your device is able to adjust the NTP time to your current local time.

The main purpose is to have a way to generate the local time zone string on the fly and not using a hard coded string (which could change over time). It also doesn't need a cloud related database of some kind. This way the functionality is self contained and not dependant upon external systems (only a working browser).

Of course the phone, tablet or computer the browser runs on should have been configured with the correct time.

## Demo/test

From VS Code open tzbuilder.html with Live Server.
