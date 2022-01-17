# TWA

 Trusted Web Activity is a new way to open your web-app content such as your Progressive Web App (PWA) from your Android app using a protocol based on Custom Tabs.

Note: Trusted Web Activity is available in Chrome on Android, version 72 and above.


https://levelup.gitconnected.com/using-trusted-web-activities-twa-with-flutter-part-1-8722c3b3979b


_There are numerous articles on the implementation of Chrome Custom Tabs and WebViews and what not. But there is not a single article or blog that states the high-level and in-depth knowledge of the Trusted Web Activities._

_With this article, I am trying to achieve this and help all the new developers in the TWA world. This article is a part of a multi-part series for understanding Trusted Web Activities._

All the parts of the TWA series:
--------------------------------

1.  Part 1: Using Trusted Web Activities with Flutter
2.  Part 2: Registering for multiple domains with Trusted Web Activities
3.  Part 3: Building communication between Trusted Web Activities and Flutter
4.  Part 4: Wrapping up

What is TWA?
============

**Trusted Web Activity** is a new way to open _your_ web-app content such as _your_ Progressive Web App (PWA) from _your_ Android app using a protocol based on Custom Tabs.

1.  Content in a Trusted Web activity is **trusted** — the app and the site it opens are expected to come from the same developer. (This is verified using [Digital Asset Links](https://developers.google.com/digital-asset-links/v1/getting-started).)
2.  The content rendered in a Trusted Web Activity comes from the **web**: they’re rendered by the user’s browser, in exactly the same way as a user would see it in their browser except they are run fullscreen. Web content should be accessible and useful in the browser first.
3.  Today, if the user’s version of Chrome doesn’t support Trusted Web activities, Chrome will fall back to a simple toolbar using a Custom Tab. It is also possible for other browsers to implement the same protocol that Trusted Web activities use. While the host app has the final say on what browser gets opened, we recommend the same policy as for Custom Tabs: use the user’s default browser, so long as that browser provides the required capabilities.

— From Android [TWA Integration guide](https://developer.chrome.com/docs/android/trusted-web-activity/overview/)

A little introduction to SkillClash TWA usage
=============================================