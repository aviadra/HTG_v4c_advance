HTG_v4c_advance
===============

Tasker profile for videoreg

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
