# Introduction #

The BeaglePod is an audio/video player for cars equipped with "IPod Ready" stereos. Using the Apple Accessory Protocol the car stereo is used to select and control the playback of media on the BeaglePod. Adding a video monitor the BeaglePod it becomes a audio/video player.  The BeadglePod is connected to the car stereo via a USB->TTL to KCE-4221 cable.  A small breadboard is used to join the two cables.


# Hardware #

  * Apline Car Stereo (Model# ??????)
  * FDTI USB TTL-RS232 USB-TTL
  * Apline KCE-422i IPod Cable
  * Breadboard with headers to join the two cable.

Why no beadgleboard listed?

Its out of stock everywhere!  In the meantime I've been using a extra VIA ITX board.

# Software #

When I first started out, it was 100% C and I hadn't heard of the beadgleboard.  Then I decided to convert it to C++ because I like objects :). Then I decided I'd use GStreamer and that lead me to GLib and callbacks. So I converted the objects back to non-objects.

# Architecture #

There are 4 components that make up the system.

  * aap - Library to manage all the serial communication and aap specific stuff
  * itunes - A library to parse itune library xml file and build playlists
  * player - A libary that delegates and controls gstreamer
  * ipod - The center hub for dispatching and connecting everything together

# Status #

Works

  * Playlist selection
  * Artist/Album/Song selection
  * Controls: Play/Pause/Next/Previous
  * Elapse time
  * Display Track Information

Not Working

  * Fast Forward/Rewind