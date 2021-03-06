# responsive emails template

This project contains an example of responsive email templates (they were used to create the giffgaff marketing emails).

You can check the templates by accessing [here](http://rafeca.com/email-templates)

# How to test

The project contains a `Rakefile` script to automate the compilation and sending of the emails
in order to ease the testing.

## Requirements

To be able to use the Rake tasks, you need to have [Ruby](http://www.ruby-lang.org/) installed.

Once it's installed, go to the folder where you have checked out this repository, and install its dependencies:

```bash
$ bundle install
```

## Sending emails

To send the basic template to any address, just execute the following:

```bash
$  rake "sendmail[youremailadress@gmail.com]"
```

To send any other email (a different html file inside the repo folder), just add the filename as the second parameter:

```bash
$  rake "sendmail[youremailadress@gmail.com,statement_points]"
```

## Building emails

You can only compile the email into a new html file without sending any email. To do so,
execute the build task witht the filename of the mail that you want to build:

```bash
$  rake "build[statement_points]"
```

The built email will be stored inside the `dist/` folder with the same file name as
the original html.

Additionally, you can build all the emails in a specific folder:

```bash
$  rake "buildall[myemails/]"
```

# Compatibility

## First-class browsers

* Gmail (Chrome 24 in OSX)
* iPhone client (iOS 7)

## Full list of tested browsers

### Mobile clients

* iPad (iOS 6.1)
* iPhone (iOS >=5.1)
* Android (2.3)
* Gmail App (iOS 5.1 in iPhone)
* Gmail App (iOS 6.1 in iPad)
* Gmail App (Android 4.0 in HTC Desire)

### Desktop clients

* Mail.app 6.2 (OSX 10.8)
* Oulook 2011 (OSX 10.8)
* Windows Live Mail 2012 (Windows 7)
* Mozilla Thunderbird 17 (Windows 7)
* Outlook Express 6.0 (Windows XP) - minor issues
* Outlook 2007 (Windows XP) - minor issues

### Web-based providers

* Gmail (Safari 6 in OSX)
* Gmail (Firefox 18 in OSX)
* Gmail (IE7/IE8 in Windows)
* Gmail Mobile (iOS 5.1 in iPhone)
* Yahoo! (Chrome 24 in OSX)
* Yahoo! (Safari 6 in OSX)
* Yahoo! (Firefox 18 in OSX)
* Yahoo! (IE7/IE8 in Windows)
* Yahoo! Mobile (iOS 5.1 in iPhone)
* live.com (Chrome 24 in OSX)
* live.com (Safari 6 in OSX)
* live.com (Firefox 18 in OSX)
* live.com (IE7/IE8 in Windows) - minor issues
* live.com Mobile (iOS 5.1 in iPhone) - minor issues

* Outlook Web App (any browser) - major issues

## Not tested yet

* Outlook 2010
* IE9/IE10
* Yahoo iOS/Android App
* Android Client 4.0, 4.1
* Blackberry
* Windows Phone 7.5/8.0
* FirefoxOS

## Known issues

### Minor bugs

- Titles in green (live.com - IE7,IE8)
- Wrong margins all across the email (live.com - IE7,IE8, mobile site)
- Margins wrong in bottom links (live.com - all browsers)
- Horizontal separators of 2px (Outlook Express)
- Lists margins are not perfect (Outlook 2007)


### Major bugs

- Bullets in lists are missplaced (Outlook Web App)
- Top navigation has no styles (Outlook Web App)
- Mobile background images not shown (Android 2.3)

### Platform problems

- The following websites show the desktop version when accessing from mobile:
  * Yahoo!
  * Gmail
  * live.com
  * GMail app in iOS
- The email is shown really big (desktop size) and can't be zoomed out (Gmail app in Android - common problem)

# LICENSE

* The giffgaff name, logo and all associated designs are property of giffgaff.com
* The HTML, CSS and Ruby code in this repository is released under the MIT license
