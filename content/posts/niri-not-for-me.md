+++
date = '2026-06-01T18:16:27+02:00'
draft = false
title = 'Niri is not for me'
+++

After a year of using Niri, I'm probably going back to Sway - here is why.

## Out of sight, out of mind

When you open four new terminal windows on Niri, you quite literally don't see the consequences. If you leave those windows at their default sizes (half screen width), you have just added 4×50%=200% (two monitors' worth) of horizontal scrolling space for your future self to sift through. You leave them there, just in case, and 'focus left' a bunch of times to return to what you were doing.

---

The time has come for you to return to one of those four windows. You are filled with anticipation - you know the terminal is in the perfect working directory, just one up-arrow away from running the command that will bring you joy.

However, you must first face your three evil exes.

You press a button, and the right half of your screen smoothly uncovers one of the terminals. Where am I? You scan the content of the terminal. This is your terminal, isn't it? So how come you don't recognize its content? You spent so much time in your IDE that you forgot what you put here. Oh right, you understand now. It's not what you're looking for.

You go to the next terminal, and your screen is now divided in half: the terminal you just passed, and a brand-new one. This one is filled with colors and text; you ran some `grep` command to find a random string. Whatever, you already resolved that, so you can close it now.

The third terminal only contains a couple of `pkill rust-analyzer` invocations and some random one-off project-related commands. Does this really need to take up 50% of your screen? At the same time, you can't put it in a tabbed column, since it's its own separate thing. You can just close it and open a fresh terminal later.

And there it is, the fourth terminal. You finally reach what you were looking for. Now imagine you already separated half of those windows into another workspace and have to deal with window-creep for each workspace separately.

## Why are you not helping me?

Web browser, terminal emulator, text editor, file browser. All of these contain their own way of separating tasks; mainly the concept of a 'tab'.

I'm reaching out to my window manager to help me unify and manage this mess. Sway spoiled me in this regard. The ability to have meticulous higher-level tabs and tiling for _any application_ is a lifesaver for people who, for whatever undiagnosed reasons, juggle a billion things in a day.

Niri simply cannot not help you manage your windows like Sway does.

## No tabs

Even though Niri [technically has a stacking layout called "Tabs"](https://niri-wm.github.io/niri/Tabs.html), it's not ideal. The indicator that a column is tabbed is borderline invisible and gives no hints as to what the contents of the other tabs are.

Furthermore, if a column is tabbed, you can't have anything else below the tabbed section. Any windows you try to put into that column will be forced to tab vertically.

In contrast, with Sway you can have the top-left corner of your screen be tabbed terminals, yet still be able to put _whatever you want_ in the bottom-left.

## Workspaces and monitors

Niri forces each workspace to live on a specific monitor. There are ways to move a workspace to another monitor, but that permanently pushes the workspace onto the other monitor's workspace stack.

Many window managers sadly force this behavior, and it adds unnecessary friction if you want to bring something up on your other monitor.

Say for example, you want to take a detour to 'like' the song you're listening to on Spotify. But wait, your Spotify is on your secondary monitor, at the bottom of the workspace stack. This means you have to switch your focus to your secondary monitor, start scrolling down[^1], find Spotify and then like the song.

However, you never find Spotify. Remember when you played a song on YouTube 3 hours ago and left the maximized YouTube window to the right of Spotify? (because they're both "music"?)
[^1]: Or hit a hotkey to take you to the last workspace; but how sure are you that your Spotify is at the very bottom? Maybe you opened something below it or relocated a workspace from your other monitor.

That is the consequence of being able to freely open windows. When you come back, you are disoriented and have to spend considerable time to figure out what you were doing. So, just scoot past YouTube, no big deal.

---

The [overview](https://github.com/niri-wm/niri/wiki/Overview) helps greatly with this, provided you hit another shortcut to bring it up, and have it zoomed out far enough to find Spotify.

---

To be fair, Sway annoyingly also doesn't have this option, but you are able to replicate it with a script such as [jschlumpp/i3-wk](https://github.com/jschlumpp/i3-wk).

This concept makes Niri's entire window searching process obsolete - if you put Spotify on workspace 5, you press the button[^2] for workspace 5 and Spotify will be brought up in front of your eyes, in plain sight.
[^2]: Niri lets you set hotkeys for specific workspaces, but this gets confusing and doesn't follow expectations: https://niri-wm.github.io/niri/Workspaces.html#addressing-workspaces-by-index

## Your Sway layout is art

A container is the building block in Sway, and it is basically a "box that contains windows or other containers".

Take the example from before:

> In contrast, with Sway you can have the top-left corner of your screen be tabbed terminals, yet still be able to put whatever you want in the bottom-left.

If you wish, you can act on all those tabbed terminals as one entity. You can stack them vertically instead, then put them into a separate new tab, which you can rename to "terminals"!

Get that: your window manager allows you to hide three full applications in the equivalent of an OS-level Firefox tab, and nothing is preventing you from making one of those containers contain three more applications.

Sway's containers and titlebars are fundamentally different to how Niri handles windows.

This is why I don't think I could ever go to a dynamic TWM again. I would highly encourage anyone to give Sway a try and see what it's capable of: https://i3wm.org/docs/userguide.html

It might not be for you, and that's okay.

## End

Niri is a great project, and YaLTeR is doing a great job polishing it. Scrolling window managers have their use and I'm positive I'll continue using Niri on my laptop where simpler things get done.

However, I find it limiting for daily use and ideally I'd like to see a mix of what makes Sway good + what makes Niri good. The `scroll` window manager forks Sway but unfortunately guts the main thing I like about it.

If you think I'm using it wrong, have questions or suggestions for me to spiral into, feel free to let me know.
