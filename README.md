<<<<<<< HEAD
graylog-UNIX-to-timestamp
=========================

## Description

A pipeline rule for graylog that takes incoming field "requestStartDateTime" which is in UNIX format and converts it
to a graylog compatible format, then overwrites the original messages "timestamp" field with this time instead.

## Usage

This works great for fetching logfiles from a CDN provider for example because they typically come delayed and this
restores the original timestamp based on the web hit vs. when the log was fetched from the message queue.

## Caveats 

This example is setup for a UNIX timestamp that only contains only seconds precision.  If the source UNIX time
is for milliseconds and you want to keep that level of precision you will need to make changes to restore that starting
with eliminating the "substring(ts, 0, -3);"
=======
# graylog-UNIX-to-timestamp
>>>>>>> 456313c640bdb3cd3d900d32efe58643e296bda8
