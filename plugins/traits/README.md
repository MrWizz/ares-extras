# Simple Traits

## Status

**Supported** Although not part of the main Ares code release, this is a supported plugin.  Report any problems you encounter: https://aresmush.com/feedback

Designed for AresMUSH 1.0

> Note: This code has been run through its paces on a test server, but hasn't been playtested on a real game yet.   The first game to implement this will receive extra technical support from Faraday to iron out any bugs.

## Overview

The traits system provides a simple way to store character stats with a name/description, as one might find on comic games.

    +==~~~~~====~~~~====~~~~====~~~~=====~~~~=====~~~~====~~~~====~~~~====~~~~~==+
    Traits - Steve
    
    Shield - Cap has a super shield.
    Strong - Cap is very strong.
    +==~~~~~====~~~~====~~~~====~~~~=====~~~~=====~~~~====~~~~====~~~~====~~~~~==+

## Installation

1. Unless you are planning to use traits in conjunction with FS3, you probably want to disable the FS3 plugins, as explained in [Enabling and Disabling Plugins](https://aresmush.com/tutorials/config/plugins/).
2. In the game, run `plugin/install traits`.

## Configuration

This plugin has no config options.

If you are using _just_ traits (without any other skills system), you probably want to alias the 'sheet' command to 'traits'.   Players usually expect 'sheet' to show them something useful.  You can do this by editing the shortcuts config in the `custom.yml` config file.

    ---
    custom:
      shortcuts:
          sheet: traits

You'll probably also want to tweak the chargen instructions.  Edit `chargen.yml` and remove these two stages:

    stages:
      sheet:
        help: sheets
      ...
      abilities:
        help: skills

Then add (in whatever position you want it to appear) a new stage:

    stages:
      ...
      traits:
        help: traits

## Web Portal

This plugin has no web portal component.
