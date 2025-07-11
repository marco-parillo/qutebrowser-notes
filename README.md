# qutebrowser-notes

## qute://settings/ 
1. auto_save.session was false. Setting it to true again takes immediate effect, no save dialogue
2. changelog_after_upgrade was minor. Shows 3.5.0. Setting it to patch shows 3.5.1
3. content.autoplay (Current: true) Try setting to false to disable autoplay
4. input.insert_mode.auto_load (Current: false) Try setting to true so when focus is on a field, you can start typing.
5. session.lazy_restore (Current: false) Try setting it to true so as not to load all tab content at startup
6. spellcheck.languages (Current: ["en-US"]) (may have to install dictionaries below first)
7. tabs.background (Current: false) so I typed true in the box to the right, but maybe tabs.background false sends tabs to background
8. tabs.mousewheel_switching (Current: true) Try setting to false so scroll always scrolls page
9. tabs.new_position.unrelated (Current: last) Try setting to next so new tabs open next
10. url.default_page (Current: https://start.duckduckgo.com/)
11. url.start_pages (Current: https://start.duckduckgo.com)

## Spell Checking
```
$ cd /usr/share/qutebrowser/scripts 
$ python dictcli.py install en-US
```
If that does not [work](https://github.com/qutebrowser/qutebrowser/issues/7481), apply this [patch](https://github.com/qutebrowser/qutebrowser/commit/f277876ce08). (sudo required).

## Turn off JavaScript?
```
:set content.javascript.enabled false
```
## Turn on Ad Block?
```
$ sudo pacman -S python-adblock
```

## Qutebrowser not respecting /etc/hosts
```
c.content.dns_prefetch = False
```
