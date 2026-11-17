# Jarvis Desktop — downloads

J.A.R.V.I.S. for your computer: the animated arc-reactor HUD, "Hey Jarvis" voice
control, weather, markets, directions, smart-home and suit control, all powered
by your own Cloudflare Worker.

## New in 1.2.3: more ways a page could reach your keyboard, closed

- When you went from **Chrome**'s address bar to the page with Escape, or a
  panel that opened and closed by itself (Spotlight, for one) gave the keyboard
  back to the page, a page in a Chrome window behind could still take the
  keyboard from the page you were typing in. It no longer can, and the keyboard
  now goes back to your page: click the field you were in to go on.
- A page that had been hidden for taking the keyboard, or one behind the lock
  screen, could still pull the keyboard to itself in a way hiding does not
  stop; in testing one read about a third of a lock-screen password. A hidden
  page that gets the keyboard again is now closed. Click its empty page to
  load it again.
- While you were in another browser tab, a page in a Chrome window behind
  could take the keyboard unseen and read what you typed when you came back.
  It is refused there too now, and the keyboard is where you left it.
- Text you drop on the address bar, a note or Spotlight while a page has the
  keyboard now takes the keyboard to that field. Before, what you typed next
  went on into the page.

## New in 1.2.2: two Chrome windows

- With two **Chrome** windows open in KODA OS, a page in the window behind can
  no longer take the keyboard from the page you are typing in. The keyboard
  then rests with the window in front; click your page to go on.
- A page you entered with Escape in the address bar can no longer pull the
  keyboard back when you Tab out of it.

## New in 1.2.1: Chrome in KODA OS keeps your keyboard yours

- A web page open in KODA OS's **Chrome** can no longer take the keyboard by
  itself while you type in the address bar, another window, Spotlight or the
  lock screen, or while you are in another app. A page that keeps trying is
  hidden until you click where it was. Chrome's **About** page states the one
  limit left.
- A link Jarvis declines to open (too long, or too many at once) is no longer
  opened in a browser tab anyway.

## New in 1.2.0: KODA OS, with Claude and Chrome

Jarvis now carries **KODA OS**, a desktop in K.O.D.A's design, inside its own
window, with **Claude** and **Chrome** preinstalled.

- **Open it** from **KODA OS**, **CLAUDE** or **CHROME** under the J.A.R.V.I.S.
  name in the HUD's top bar, by saying *"open KODA OS"* or *"open Claude"*, or
  at http://127.0.0.1:8090/os/ in any browser on the same computer while Jarvis
  runs. **Jarvis HUD** in KODA OS's menu brings the dashboard back.
- **Claude** uses **your own Anthropic API key** (from console.anthropic.com).
  The key and your conversations stay on your computer, and the key is sent
  only to Anthropic.
- **Chrome** shows the sites that allow being shown inside another page; for
  the rest (many large sites), **Open in a New Tab** opens the page in your
  default browser.
- What KODA OS saves (settings, the Claude key and chats, bookmarks) is kept
  between runs.

## Download

Grab the newest installer from **[Releases → Latest](../../releases/latest)**:

| Computer | File |
| --- | --- |
| Windows 10 / 11 | `JarvisSetup-<version>.exe` |
| Mac with Apple silicon (M1–M4) | `Jarvis-<version>-arm64.dmg` |
| Mac with an Intel chip | `Jarvis-<version>-x86_64.dmg` |
| Linux | `Jarvis-<version>-linux-x86_64.tar.gz` |

## Install

- **Windows:** run the installer. It installs for your user (no admin prompt) and
  adds Start Menu and desktop shortcuts. If SmartScreen says *Windows protected
  your PC*, click **More info → Run anyway** — the build is not code-signed yet.
- **macOS:** open the disk image and drag **Jarvis** to **Applications**. The
  first time, **right-click Jarvis → Open → Open**. If macOS insists the app is
  "damaged", run once in Terminal: `xattr -dr com.apple.quarantine /Applications/Jarvis.app`
- **Linux:** unpack the tarball and run `Jarvis/Jarvis`.

## First launch

Jarvis opens on a setup screen. Paste your Worker URL and `JARVIS_API_KEY`,
pick a city for the weather panel and the tickers you want, and press **Bring
Jarvis online**. It downloads the speech model once (about 150 MB) and asks for
microphone access. Change any of it later from **⚙ SETTINGS** in the HUD's top
bar, and change the look from the **UI Studio** at http://127.0.0.1:8090/editor
while Jarvis is running. KODA OS, with Claude and Chrome, is one click away in
the same top bar.

---

Builds are published automatically from the private source repository. This
repository holds the installers only.
