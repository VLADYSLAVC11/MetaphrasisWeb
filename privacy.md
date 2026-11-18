---
layout: default
title: Privacy Policy
permalink: /privacy/
description: What Metaphrasis does with your information, and what it never does.
---
{% assign m = site.metaphrasis %}

# Privacy Policy

<p class="effective">Effective {{ m.policies_effective }}</p>

Metaphrasis is a translation app for iPhone and iPad, published by
{{ m.publisher }} ("we", "us"), an individual developer in {{ m.governing_law }}.
This policy explains what happens to your information when you use the app,
Metaphrasis Cloud, and this website.

<div class="summary" markdown="1">

**The short version**

- There is no account. We never learn your name, email address or payment
  details.
- Translation and speech recognition on your device send nothing anywhere.
- **Basic and Premium** add Metaphrasis Cloud. When you use it, your text or
  voice goes to the service doing the work (Google, Deepgram or ElevenLabs).
  Our server keeps how much you used, never what you said or translated.
- **Free** shows ads from Google, which receives what an ad needs, never
  what you translate or say.
- A **Private** conversation never uses any cloud service.

</div>

## What stays on your device

What you type or say, and its translation, is not saved. Conversations are
kept only while they last; share or copy one before ending it if you want it.
The app keeps your settings and the favorites you choose to save, in its own
storage on your device. Favorites are included in your device backups, like
other app data. Downloaded language packs and speech models are not.

Photos taken or picked for camera translation are read on your device and
never saved or sent anywhere. Photos are picked through iOS's own picker, so
Metaphrasis has no access to your photo library.

API keys you add for DeepL or Google are kept in your device's Keychain. They
are not synced through iCloud, are not restored to another device from a
backup, and are sent only to the service they belong to.

## What the app asks permission for

- **Microphone**: to hear what you say and translate it.
- **Speech recognition**: to turn what you say into text.
- **Camera**: to read text and translate it.
- **Local network**: to find a nearby phone for a conversation across two
  phones.
- **Tracking** (Free only): to let the ads you see be chosen for you. You see
  ads either way.

Each is asked only when you first use the feature that needs it, and can be
changed in the iPhone's Settings app under Metaphrasis.

## When information leaves your device

### Apple speech recognition and downloads

For a language your device cannot recognise on its own, iOS may send the audio
to Apple's servers to be transcribed. This is on by default. Turn off **Use
Apple servers** in Settings › Speech Recognition to keep recognition on your
device. A **Private** conversation always recognises speech on the device,
whatever that setting says. Apple handles this audio under the
[Apple Privacy Policy](https://www.apple.com/legal/privacy/), and we do not
receive it.

Apple's on-device translation languages, and the Enhanced and Premium voices
that read translations aloud, are downloaded from Apple.

### DeepL and Google with your own API key (optional)

This is off unless you add your own DeepL or Google API key and turn on cloud
translation. The text you translate is then sent from your device directly to
DeepL or Google, under your own account with them. It does not pass through
us, and we never see it. Saving a key sends a short test translation to check
that the key works.

How DeepL or Google store and use that text depends on your agreement with
them, including the plan your key belongs to. See the
[DeepL Privacy Policy](https://www.deepl.com/privacy) and the
[Google Cloud Privacy Notice](https://cloud.google.com/terms/cloud-privacy-notice).

### Metaphrasis Cloud (Basic and Premium)

Metaphrasis Cloud is our own service. It adds cloud speech recognition,
translation and voices to a paid plan. It is used only on a paid plan, never
in a Private conversation, and each part can be turned off in the app's
Settings.

**How it knows your plan.** There is no sign-in. The app proves your
subscription with the signed transaction the App Store gave it, and proves
it is the genuine Metaphrasis app with Apple's App Attest. Our server
receives the subscription's App Store transaction number, which product it
is, when it expires, and a device key that App Attest created for the app.
Nothing in it names you.

**Translation.** The text you translate, with the sentence before it for
context, passes through our server to Google's Gemini API, and its
translation comes back. Our server does not log or keep the text. We use
Google's paid service, under which Google does not use it to improve its
products. Google may keep it for a limited time to detect abuse, under its
[Gemini API terms](https://ai.google.dev/gemini-api/terms).

**Cloud speech recognition** is off until you turn on **Metaphrasis Cloud**
in Settings › Speech Recognition. While it is on, what you say is streamed
from your device directly to Deepgram's servers in the EU, from the moment a
voice is heard until the microphone closes. Our server only gives your
device a short-lived permission to connect, and learns how long the session
ran. It never receives the audio or its transcript. The app opts out of
Deepgram using the audio to improve its models. See the
[Deepgram Privacy Policy](https://deepgram.com/privacy).

**Cloud voices** (Premium) read a translation aloud. The text to be read
passes through our server to ElevenLabs, and the audio comes back through
it. Our server does not log or keep the text or the audio. ElevenLabs
processes it under the
[ElevenLabs Privacy Policy](https://elevenlabs.io/privacy-policy). The voice
previews in the app are recordings and send nothing about you.

**What our server keeps:**

| What | How long |
|---|---|
| Your subscription: its App Store transaction number, product, status and expiry | Until 12 months after the subscription ends |
| Each device's App Attest key, and when it was last seen | Until 12 months after the subscription ends, or after the device was last seen |
| How much of each allowance a period has used | Until 12 months after the subscription ends |
| For each request: when, which device, and how many seconds, words or characters it used | 90 days |

It does not record your IP address, and it keeps no text and no audio. The
server runs on [Fly.io](https://fly.io/legal/privacy-policy/) in Frankfurt,
Germany.

### Ads on the Free plan

The Free plan shows ads from Google AdMob. Basic and Premium do not load
Google's ad software at all.

To show and measure ads, Google receives this device's identifiers, its
approximate location from its IP address, how ads are seen and tapped, and
diagnostic data about the ad software. Ad requests never contain what you
translate, say or photograph, or which languages you use.

The first time an ad could be shown, users in the EEA, the UK and Switzerland
are asked whether Google may use their data for personalised ads, and users in
US states with privacy laws are shown the matching notice. Then iOS asks
whether the app may track you. Google receives the advertising identifier only
if you allow it. Without it, you still see ads, just less relevant ones. You
can change your choices at any time in the app under Settings › Privacy &
Security › Ad Privacy Choices, and in iOS under Settings › Privacy & Security ›
Tracking.

Ads are limited to those suitable for general audiences. Google handles this
data under its [Privacy Policy](https://policies.google.com/privacy); see also
[how Google uses information from apps that use its services](https://policies.google.com/technologies/partner-sites).

### Language pack and speech model downloads

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

## Purchases

Subscriptions are bought, renewed, cancelled and refunded through the App
Store. Apple handles the payment, and we never see your name, email address or
payment details. We receive only the transaction information described under
Metaphrasis Cloud.

## Who else handles your information

| Who | What for | When |
|---|---|---|
| Apple | speech recognition on its servers, downloads, App Store purchases, App Attest | as described above |
| Google (Gemini API) | Metaphrasis Cloud translation | Basic and Premium, with cloud translation on |
| Deepgram | Metaphrasis Cloud speech recognition | Basic and Premium, with cloud speech on |
| ElevenLabs | Metaphrasis Cloud voices | Premium, with cloud voices on |
| Google (AdMob) | ads | Free |
| Fly.io | hosting our server | Basic and Premium |
| Google Drive | language pack and model downloads | when you download one |
| DeepL, Google Cloud Translation | translation under your own key | only if you add one |
| GitHub | hosting this website | when you visit it |

We do not sell information about you. The only information shared for
advertising is what Google's ad software receives on the Free plan, as
described above.

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

## Legal bases

Where the EU or UK General Data Protection Regulation applies, we rely on:

- **performance of a contract** to provide Metaphrasis Cloud on the plan you
  bought, and to answer your questions;
- **your consent** for personalised ads and tracking on the Free plan, which
  you can withdraw at any time as described above;
- **our legitimate interests** in showing non-personalised ads on the Free
  plan, and in protecting Metaphrasis Cloud from abuse (App Attest, usage
  limits).

We also process personal data in line with the Law of Ukraine "On Personal
Data Protection".

Our server is in Germany, we work from {{ m.governing_law }}, and some of the
services named above process data in the United States and elsewhere. Where
the GDPR applies, transfers rely on those services' own safeguards, such as
the European Commission's Standard Contractual Clauses.

## Your choices and rights

Deleting the app removes its data from your device. Remove your API keys first
in Settings › Privacy & Security: iOS can keep Keychain items after an app is
deleted.

Depending on where you live, you may have the right to access, correct or
delete personal data held about you, to object to or restrict its use, and to
receive a copy of it. To use them, write to
[{{ m.contact_email }}](mailto:{{ m.contact_email }}). To find your Metaphrasis
Cloud records, include the **Order ID** from the App Store receipt email for
your subscription: it lets us find the subscription without knowing who you
are. We answer within one month.

You can also complain to a data protection authority: in the EU, the one where
you live; in Ukraine, the Ukrainian Parliament Commissioner for Human Rights.

**US state privacy rights.** Some US state laws treat the ads on the Free plan
as "sharing" personal information for targeted advertising. You can opt out in
the app under Settings › Privacy & Security › Ad Privacy Choices, or by not
allowing tracking. Basic and Premium share nothing for advertising.

## Children

Metaphrasis is not directed at children under 13, or under the age of digital
consent where you live, and we do not knowingly collect their information. Ads
on the Free plan are limited to those suitable for general audiences. If you
believe a child has sent us personal information, write to us and we will
delete it.

## This website

This website is hosted on GitHub Pages. GitHub may record visitors' IP
addresses to keep the service secure; see the
[GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
The site itself sets no cookies, uses no analytics, and loads nothing from
any other website.

## Changes to this policy

If this policy changes, the new version will be published here with a new
effective date, and a change that matters will be mentioned in the
[release notes]({{ '/releases/' | relative_url }}).

## Contact

{{ m.publisher }}, {{ m.governing_law }}<br>
[{{ m.contact_email }}](mailto:{{ m.contact_email }})
