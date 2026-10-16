# SpareScreen

Use any spare tablet, phone or laptop with a browser as a wireless second screen for your Mac.

SpareScreen sits in the menu bar. Open its link on your tablet and the Mac gets an extra screen in the
tablet's exact shape. Drag windows onto it like any monitor. Close the page and the screen disappears.
You don't install anything on the tablet.

## Install

```sh
brew tap chaibreak/tap; brew trust --tap chaibreak/tap; brew install --cask sparescreen && open -a SpareScreen
```

SpareScreen then opens in the menu bar. Free for 7 days; a one-time license is on [getsparescreen.com](https://getsparescreen.com).

Or download it from [getsparescreen.com](https://getsparescreen.com) (or `SpareScreen-<version>.zip` from
[Releases](https://github.com/chaibreak/sparescreen/releases)) and move **SpareScreen.app** to your Applications folder.

### First launch: "Open Anyway" (download only)

Homebrew installs open straight away. SpareScreen isn't signed by Apple, so a downloaded copy is blocked the first time:

1. Open SpareScreen. macOS says it can't be opened. Click **Done**.
2. Go to **System Settings → Privacy & Security**, scroll down, and click **Open Anyway** next to SpareScreen.
3. Confirm with **Open**.

You only do this once per version.

## Set up

1. **Allow Screen Recording.** SpareScreen asks on first launch. Turn it on under **System Settings → Privacy &
   Security → Screen & System Audio Recording**, then quit and reopen SpareScreen. macOS needs this permission to
   let SpareScreen show what's on the extra screen.
2. **Connect the tablet.** Make sure the tablet is on the same Wi-Fi as the Mac. Click the SpareScreen icon in the
   menu bar and scan the QR code with the tablet, or type the link into its browser.
3. **Allow the tablet.** The Mac asks whether this tablet may show your screen. Click **Allow**. SpareScreen
   remembers it.

Tap the tablet's screen once to go full screen. To place the tablet left or right of your Mac, use
**System Settings → Displays → Arrange**.

## Using it

- **Connecting and disconnecting is automatic.** The extra screen appears when the tablet opens the link. It's
  removed 15 seconds after the tablet goes away (page closed, screen off, Wi-Fi lost), and your windows move back
  to the main screen.
- **Rotate the tablet** and the extra screen follows after a few seconds.
- **Pause:** use **Pause sharing** in the menu, or macOS's **Stop Sharing**. **Resume** brings the screen back.
- **Text size:** Larger, Default, or More space.
- **Picture:** Faster (less data, softer), Balanced, or Sharper.
- **Open at Login:** starts SpareScreen when you log in.
- **Forget Allowed Tablets:** every tablet has to be allowed again.

The dot in the tablet's corner is green while it's connected and red when it isn't. A message says why: the Mac
isn't reachable, sharing is paused, the tablet needs approval, or permission is missing.

## Good to know

- **Use it on Wi-Fi you trust.** The picture travels unencrypted over your local network. The link contains a
  secret key and new tablets have to be allowed on the Mac, but someone on the same network with the right tools
  could still watch the traffic.
- **Screen Recording carries over to updates** from version 1.0.5. Updating from an older version needs it allowed
  once more: remove the old SpareScreen entry under Screen & System Audio Recording, then allow the new one.
- **No touch input.** The tablet shows the screen. You control it with the Mac's mouse and keyboard.
- **Video and fast scrolling are the heaviest.** Cursor moves and typing send only the part of the screen that
  changed, so they're light.
- **It relies on a private macOS feature.** That feature creates the extra screen, and the same approach is used
  by BetterDisplay and DeskPad. A future macOS update could break it.
- Requires macOS 13 (Ventura) or later, on Apple Silicon or Intel.

