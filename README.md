# qutebrowser-notes

## qute://settings/ 
1. auto_save.session was false. Setting it to true again takes immediate effect, no save dialogue.
1. input.insert_mode.auto_load (Current: false) Try setting to true so when focus is on a field, you can start typing.
1. session.lazy_restore (Current: false) Try setting it to true so as not to load all tab content at startup
1. spellcheck.languages (Current: ["en-US"]) (may have to install dictionaries below first)
1. tabs.background (Current: false) so I typed true in the box to the right, but maybe tabs.background false sends tabs to background
2. tabs.mousewheel_switching (Current: true) Try setting to false so scroll always scrolls page
3. tabs.new_position.unrelated (Current: last) Try setting to next so new tabs open next
4. url.default_page (Current: https://start.duckduckgo.com/)
5. url.start_pages (Current: https://start.duckduckgo.com)

## Spell Checking
```
$ cd /usr/share/qutebrowser/scripts 
$ python dictcli.py install en-US
```

## Turn off JavaScript?
```
:set content.javascript.enabled false
```
