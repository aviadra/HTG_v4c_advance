HTG_v4c_advance
===============

Tasker profile for videoreg

v1.4
Behavior change: VideoReg is no longer stopped when a phone call is in progress.
Pre v1.4, the car mode profile was set to disable video recording during a phone call. This was done to reduce the interruption of a conversation, when the video clip rotated as the media route would toggle between the internal speacker+mic to the BT one. 
With the above stated, many changes were introduced to indeed keep the video recording toggle outside of the 10m interval.

Assumption change: From v1.4 and beyond, it is assumed that Videoreg is set to make longer intervals between clips (I use 10m), so that the media toggle would normally happen outside of the regular duration of a call and/or would be not as disruptive to the conversation. 
Added: “Reset Record” profiles that restart the video recording, so that it would get the full 10 minutes count when a phone call is ongoing. The reset is triggered by: opening the phone app, receiving/making a call, answering a call and a very long “save on 3”.
Added: “Convert app to event” profile, that overcomes the ambiguity of when did the “Samsung phone” app started as it lingers in memory and prevents Tasker from clearly defining its state. I’ve later used it for the exDialer app, just to preserve behavior consistency.
Added: Cooldown variable to serve as a common back-off bus for tasks.
Changed: “Save on 3” now also resets the video recording if held for longer than 5 seconds.
Changed: If a restart recording was triggered by a long “save on 3”, there is a “say” notification.
Fixed: v4c toggler was not toggeling all the new profiles created post v1.3
Changed: Video recording profile now stops if power is les then 25%.
Added: When Video recording is started, it first checks there is at least 35% power.

v1.3
Fixed: task "videoreg toggler" incorrectly toggling the “on phone”
profiles on incoming call, causing the post call delay to not work.
Changed: "videoreg toggle" task to have debugging msgs if “debug”
variable contains “v4c”.
Changed: "videoreg toggle" to have a larger delay after ending a call.
Added: variable “HTG_CAR_TALK”, to toggle verbal feedback.
Changed: Increased verbal feedbacks.

Version 1.2
Fixed: task "videoreg toggler" incorrectly toggling the “on phone” profiles on incoming call, causing the post call delay to not work.
Changed: "videoreg toggle" task to have debugging msgs if “debug” variable contains “v4c”.
Changed: "videoreg toggle" to have a larger delay after ending a call.
Added: variable “HTG_CAR_TALK”, to toggle verbal feedback.
Changed: increased verbal feedbacks.


Version 1.2
Change: Gave car-mode profile higher priority.
Change: Made “save on 3” task, capture a picture and “say” what action has been performed.
Added: Triggers for “widget locker” and ”poweramp” to be launched when entering car-mode. (If you don’t have these programs, you may delete these triggers).
Added: The v4c profile now checks for a “phone call” state, so that it natively stops during a call, and doesn’t just wait for the profile to be disabled by the “phone call” profiles.


Version 1.1a - moved to github.

Version 1.1 -	Bugfix – Receiving a call re-enables video recording, regardless of if it was disabled manually.
		Changed – The “say” statements to represent the HTG version and not the Hotfortech generation.
		Changed – Obfuscated some Hotfortech personal info.
		Changed – exit car mode sends a “stop videoreg” in the hopes of solving a bug where even if “v4c” is disabled, the camera app doesn’t work until you manually enter videoreg and exit it (or simply reboot) to release the camera device.


Version 1.0 - Init release with the hopes that it is found useful.
