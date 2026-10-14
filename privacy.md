---
layout: default
title: Privacy Policy
permalink: /privacy/
description: What Metaphrasis does with your information — which, for the most part, is nothing at all.
---
{% assign m = site.metaphrasis %}

# Privacy Policy

<p class="effective">Effective {{ m.policies_effective }}</p>

Metaphrasis is a translation app for iPhone and iPad, published by {{ m.publisher }}
("we", "us"). This policy explains what happens to your information when you use
the app and this website.

<div class="summary" markdown="1">

**The short version**

- We do not collect information about you through the app. There is no account,
  no analytics, no advertising and no tracking, and no server of ours that your
  words or your voice pass through.
- Most translation and speech recognition happens on your device.
- Some features use Apple, DeepL or Google. When they do, your text or audio
  goes to them, not to us, and their privacy policies apply.
- We receive information only when you choose to send it to us: a support
  question, a review, or a crash report you have agreed to share.

</div>

## What stays on your device

What you type or say, and its translation, is not saved; the app keeps only
the favorites you choose to save, and your settings. Both stay in the app's
storage on your device. Favorites are included in your device backups, like
other app data; downloaded language packs and speech models are not.

API keys you add for DeepL or Google are kept in your device's Keychain. They
are not synced through iCloud, are not restored to another device from a
backup, and are sent only to the service they belong to.

## When information leaves your device

### Apple speech recognition

When you speak, Metaphrasis can use Apple's speech recognition. For a language
your device cannot recognise on its own, iOS may send the audio to Apple's
servers to be transcribed. Apple handles it under the
[Apple Privacy Policy](https://www.apple.com/legal/privacy/). We do not receive
the audio or the transcript from Apple.

You can keep recognition on your device: turn off **Use Apple servers** in
Settings › Speech Recognition. A conversation started as **Private** always
recognises speech on the device, whatever that setting says.

Apple's on-device translation runs on your device. Its language downloads come
from Apple.

### DeepL and Google cloud translation (optional)

Cloud translation is off unless you add your own DeepL or Google API key and
turn it on. When it is used, the text you translate is sent from your device
directly to DeepL or Google, under your own account with them. It does not
pass through us, and we never see it. Saving a key sends a short test
translation to check that the key works.

How DeepL or Google store and use that text depends on your agreement with
them, including the plan your API key belongs to. DeepL, for example, may use
text sent with a free API key to train its models, but does not keep text sent
with a paid one. See the
[DeepL Privacy Policy](https://www.deepl.com/privacy) and the
[Google Cloud Privacy Notice](https://cloud.google.com/terms/cloud-privacy-notice).

Private conversations never use cloud translation.

### Language pack downloads

Metaphrasis language packs and speech models are downloaded from the file host
we publish them on (Google Drive at present). As with any download, the host
sees your device's IP address. Nothing else about you is sent.

### Conversations across two phones

Two phones in a conversation connect directly to each other, over Wi-Fi or
Bluetooth, with an encrypted connection. What is said passes between the two
phones only, never through a server. Nothing is kept after the conversation
ends.

So that the second phone can find the first, the phone that starts a
conversation announces to nearby devices running Metaphrasis the name you gave
it (such as "Alex's iPhone"), the conversation's two languages, and whether it
is Private. It keeps announcing while the conversation lasts, so that a partner
who drops out can rejoin, and stops when the conversation ends.

## Information you choose to send us

**Support questions.** If you write to us, we receive your email address and
whatever you include, such as the app version you copy from About. We use it
only to answer you, keep it only as long as that takes, and never share or sell
it.

**Reviews.** Ratings and reviews on the App Store are published by Apple under
the name you choose there. We see them as anyone does, and may reply to them in
the App Store.

**Crash reports.** Metaphrasis contains no crash-reporting or analytics
software of its own. If you have turned on **Share With App Developers** in
Settings › Privacy & Security › Analytics & Improvements, Apple may pass us
crash reports and diagnostics from the app. They describe the failure (device
model, iOS version, and where in the app it happened) and do not identify you.
We use them only to fix problems. If you test a beta through TestFlight,
feedback you send through TestFlight reaches us with the details TestFlight
shows you before sending.

## What we do not do

We do not sell or rent information, show advertising, track you across other
companies' apps or websites, or build a profile of you.

## This website

This website is hosted on GitHub Pages. GitHub may record visitors' IP
addresses to keep the service secure; see the
[GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
The site itself sets no cookies and uses no analytics, and loads nothing from
any other website.

## Children

Metaphrasis does not collect personal information from anyone, children
included.

## Your choices and rights

Deleting the app removes its data from your device. Remove your API keys first
in Settings › Privacy & Security: iOS can keep Keychain items after an app is
deleted.

Depending on where you live, you may have the right to access, correct or
delete personal data held about you. The only personal data we hold is
correspondence you have sent us; to see it or have it deleted, write to
{{ m.contact_email }}.

## Changes to this policy

If this policy changes, the new version will be published here with a new
effective date, and a change that matters will be mentioned in the
[release notes]({{ '/releases/' | relative_url }}).

## Contact

{{ m.publisher }}<br>
{{ m.contact_email }}
