---
layout: post
title: A recipe for recording videos (frequently updated)
date: 2024-08-03
---

Recording research videos is still a challenging task to me. You have to use an arsenal of tools to improve the quality of their recordings.

## Recording the video
For that, I use the [OBS studio](https://obsproject.com/) program, setting the scene before starting the recording. For the microphone, there is a gauge that is really helpful in konwing whether the placement of the microphone is suitable for the recording.

## Editting the video
[Shotcut](https://www.shotcut.org/) is a video editting software that so far has proven to be enough for my recordings. I use the following features of it:
* Splitting the recordings to cut-off any extended durations of silence.
* Merging multiple videos into a single video, while using the `fade-in` and `fade-out` features for making the transitions more natural.
* Applying sound filters to remove any noise caused by the microphone.
* Using the `Size, Position & Rotate` video filter for controlling the position of the video. This is useful for adding a black strip at the bottom of the video, on which subtitles can be overlayed later.

## Adding subtitles to your video
Youtube provides a really convenient way for automatically generating captions, and providing a way to post-edit them, in addition to the option of exporting the subtitles in the .srt format.

Afterward, I used the [handbrake](https://handbrake.fr/) program to overlay the subtitles on top of the recorded video. Make sure to disable the `Cropping` option which automatically crops out any black boundaries of the video.