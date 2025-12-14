--- WORKING COPY ---

[Version 1.1.0 Beta]

Version history for Are You LIVE? (AYL)


1.1.0 Beta (closed) [ Modernize all the things update ]:

  Additions:

  - Added 🧪 emoji to testers.
  - Default Dark theme.
  - New "gear" menu. 
  - Support for future custom themes.
  - Support for multiple lists.
  - Manual Save and Save As menu options.
  - Solar‑powered night mode. Works best in total darkness.
  - Support for Importing and Exporting Lists.
  - Option to delete a channel list, except 'default' and the currently loaded one.
  - Migrate old channel list save file to the new .aylc file type to support multiple save files and sharing.
  - Channel list name (and size) where the old buttons were.

  Changes:
  - Moved to a modern GUI library to allow much more customization.
  - Lists no longer auto save when making a change. Instead, the name of the list turns color (red by default), reminding you to save it.
  - Moved buttons from the top to the new "gear" menu.
  - Channel list files now use a custom .aylc file extension. 
  - You can now hit 'enter' after typing in a new channel name. (Requested by ExplodinBeef)
  - Improved the efficiency of the initial sync process, making it about twice as fast.
  - Removed 'Bifsie' channel respawn.
  - Removed Easter Eggs.
  - Moved 'Remove Channel' button to a right click on the channel.

  Fixes:
  - Network threads were not being released after refresh, causing errors after many hours of runtime. They are now in a single thread.
  - Update worker now dies and rebuilds every 15 minutes (or sooner) to prevent a stale connection and built up threads.
  - Refactored the update loop to prevent hammering of Kick's resources. We only check uptime once when a channel goes from offline -> online then tick the uptime counter internally.
  - Refactored the handling of 502 errors from Kick's API. Now we ignore it and try again during the next update cycle. Banned/removed/not found channels (404) are still flagged as 'Not Found' in the GUI.
  - Sent Herobrine to Mars to start a colony.
  - Refactored the backend code. RAM now gets released as it should. There is no longer a need to shut it down when you sleep.

  Notes:
  - If you run a prior version after running this one, you will get an odd 'new version' behavior and an orphaned duplicate channel list. You are not meant to go backward in the closed beta releases. This is because of how I am handling versioning at the moment. This will not break your channel list.
