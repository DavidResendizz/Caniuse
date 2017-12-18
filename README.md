Caniuse
===========

Just what you've always wanted, it's a `caniuse` command line tool!
All the power of [caniuse.com](http://caniuse.com) with none of the nice UI or interactivity!


How do?
-------

Install with Snap typing `sudo snap install caniuse`.

Then type things like this:

```
$ caniuse websockets
Web Sockets ✔ 85.22% ◒ 1.35% [W3C Candidate Recommendation]
  Bidirectional communication technology for web apps #JSAPI

  IE ✘ 5.5+ ✔ 10+
  Firefox ✘ 2+ ◒ 4+¹ ◒ 6+ᵖ² ✔ 11+
  Chrome ◒ 4+¹ ◒ 15+² ✔ 16+
  Safari ✘ 3.1+ ◒ 5+¹ ◒ 6+² ✔ 7+
  Opera ✘ 9+ ◒ 11+¹ ✔ 12.1+

    ¹Partial support refers to the websockets implementation using an older version of the protocol and/or the
    implementation being disabled by default (due to security issues with the older protocol).
    ²Partial support refers to lacking support for binary data.
```

(The output has truly marvellous colours that this markdown is too narrow to contain.)

Or this:

```
$ caniuse input
caniuse input
HTML5 form features ✔ 4.21% ◒ 82.39%
  IE ✘ 5.5+ ◒ 10+ Firefox ✘ 2+ ◒ 4+ Chrome ◒  Safari ✘ 3.1+ ◒ 4+ Opera ✔ 9+ ◒ 15+
Spellcheck attribute ✔ 60.31% ◒ 31.63%
  IE ✘ 5.5+ ✔ 10+ Firefox ✔  Chrome ✘ 4+ ✔ 9+ Safari ✘ 3.1+ ✔ 5.1+ Opera ✘ 9+ ✔ 10.5+
Range input type ✔ 87.46% ◒ 1.18%
  IE ✘ 5.5+ ✔ 10+ Firefox ✘ 2+ ✔ 23+ Chrome ‽ 4+ ✔ 5+ Safari ✔  Opera ✔
Date and time input types ✔ 60.76% ◒ 0%
  IE ✘  Firefox ✘  Chrome ✘ 4+ ✔ 20+ Safari ✘  Opera ✔
Color input type ✔ 60.93% ◒ 3.84%
  IE ✘  Firefox ✘ 2+ ✔ 29+ Chrome ✘ 4+ ✔ 20+ Safari ✘  Opera ✘ 9+ ✔ 11+ ✘ 15+ ✔ 17+
Number input type ✔ 49.95% ◒ 38.03%
  IE ✘ 5.5+ ◒ 10+ Firefox ✘ 2+ ✔ 29+ Chrome ✘ 4+ ✔ 6+ Safari ✘ 3.1+ ✔ 5+ Opera ✔
input placeholder attribute ✔ 88.04% ◒ 1.15%
  IE ✘ 5.5+ ✔ 10+ Firefox ✘ 2+ ✔ 4+ Chrome ✔  Safari ◒ 3.1+ ✔ 5+ Opera ✘ 9+ ◒ 11+ ✔ 11.5+
Pointer events ✔ 8.5% ◒ 1.67%
  IE ✘ 5.5+ ◒ 10+ᵖ ✔ 11+ Firefox ✘  Chrome ✘  Safari ✘ 3.1+ ‽ 6.1+ Opera ✘
Web Speech API
  IE ✘  Firefox ✘  Chrome ✘ 4+ ◒ 25+ᵖ Safari ✘ 3.1+ ◒ 6.1+ᵖ ◒ 7.1+ Opera ✘
Multiple file selection ✔ 67.63% ◒ 0%
  IE ✘ 5.5+ ✔ 10+ Firefox ✘ 2+ ✔ 3.6+ Chrome ✘ 4+ ✔ 5+ Safari ✘ 3.1+ ✔ 4+ Opera ✘ 9+ ✔ 10.6+
Gamepad API ✔ 46.08% ◒ 0%
  IE ✘  Firefox ✘ 2+ ✔ 29+ Chrome ✘ 4+ ✔ 21+ᵖ ✔ 25+ Safari ✘  Opera ✘ 9+ ✔ 24+
Pattern attribute for input fields ✔ 72.88% ◒ 0.7%
  IE ✘ 5.5+ ✔ 10+ Firefox ✘ 2+ ✔ 4+ Chrome ✘ 4+ ✔ 10+ Safari ✘  Opera ✘ 9+ ✔ 9.5-9.6+
```

Does it have lots of command line options?
------------------------------------------

Yes!

```
$ caniuse --help
Options:
Options:
  --short, -s            Short output: show browsers on one line and don't
                         display notes or description (default when displaying
                         multiple results)                             [boolean]
  --long, -l             Long output: show more information (default when
                         displaying a single result)                   [boolean]
  --oneline, -1          One-line output: just global percentages, no per-
                         browser info                 [boolean] [default: false]
  --oneline-browser, -2  One-line output with browser info, implies --abbrev and
                         --current                    [boolean] [default: false]
  --abbrev, -a           Abbreviate browser names     [boolean] [default: false]
  --percentages, -p      Include browser version usage percentages
                                                      [boolean] [default: false]
  --future, -f           Include future browser versions
                                                      [boolean] [default: false]
  --current, -c          Don't include old browser versions, equivalent to --era
                         e0                           [boolean] [default: false]
  --era, -e              How many versions back to go, e0 to e-40       [string]
  --mobile, -m           Include mobile browsers      [boolean] [default: false]
  --desktop, -d          Include desktop browsers      [boolean] [default: true]
  --browser, -b          Show results for these browsers, comma-separated (ie,
                         edge,firefox,chrome,safari,opera,ios_saf,op_mini,
                         android,bb,op_mob,and_chr,and_ff,ie_mob,and_uc)
                                                                        [string]
  --web, -w              Go to the search page on caniuse.com
                                                      [boolean] [default: false]
  --config, -C           Path to JSON config file
                                 [string] [default: "/Users/user/.caniuse.json"]
  --ascii, -A            UTF-8 symbols replacement with ASCII description
                                                      [boolean] [default: false]
  --help                 Show help                                     [boolean]

```


## Remaining tasks

Snapcrafters ([join us](https://forum.snapcraft.io/t/join-snapcrafters/1325)) 
are working to land snap install documentation and
the [snapcraft.yaml](https://github.com/snapcrafters/fork-and-rename-me/blob/master/snap/snapcraft.yaml)
upstream so [Project] can authoritatively publish future releases.

  - [x] Fork the [Snapcrafters template](https://github.com/snapcrafters/fork-and-rename-me) repository to your own GitHub account.
    - If you have already forked the Snapcrafter template to your account and want to create another snap, you'll need to use GitHub's [Import repository](https://github.com/new/import) feature because you can only fork a repository once.
  - [ ] Rename the forked Snapcrafters template repository
  - [ ] Update logos and references to `[Project]` and `[my-snap-name]`
  - [ ] Create a snap that runs in `devmode`
  - [ ] Register the snap in the store, **using the preferred upstream name**
  - [ ] Add a screenshot to this `README.md`
  - [ ] Publish the `devmode` snap in the Snap store edge channel
  - [ ] Add install instructions to this `README.md`
  - [ ] Update snap store metadata, icons and screenshots
  - [ ] Convert the snap to `strict` confinement, or `classic` confinement if it qualifies
  - [ ] Publish the confined snap in the Snap store beta channel
  - [ ] Update the install instructions in this `README.md`
  - [ ] Post a call for testing on the [Snapcraft Forum](https://forum.snapcraft.io) - [link]()
  - [ ] Ask a [Snapcrafters admin](https://github.com/orgs/snapcrafters/people?query=%20role%3Aowner) to fork your repo into github.com/snapcrafters, transfer the snap name from you to snapcrafters, and configure the repo for automatic publishing into edge on commit
  - [ ] Add the provided Snapcraft build badge to this `README.md`
  - [ ] Publish the snap in the Snap store stable channel
  - [ ] Update the install instructions in this `README.md`
  - [ ] Post an announcement in the [Snapcraft Forum](https://forum.snapcraft.io) - [link]()
  - [ ] Submit a pull request or patch upstream that adds snap install documentation - [link]()
  - [ ] Submit a pull request or patch upstream that adds the `snapcraft.yaml` and any required assets/launchers - [link]()
  - [ ] Add upstream contact information to the `README.md`  
  - If upstream accept the PR:
    - [ ] Request upstream create a Snap store account
    - [ ] Contact the Snap Advocacy team to request the snap be transferred to upstream
  - [ ] Ask the Snap Advocacy team to celebrate the snap - [link]()

If you have any questions, [post in the Snapcraft forum](https://forum.snapcraft.io).
