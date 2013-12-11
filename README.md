webrtc-based-android-aecm
=========================

  Java API for android acoustic echo cancellation.
  
  I already tested and using it on a LAN demo several monthes ago, it worked well most of the time but sometimes with little feedback, I know there must have something todo to make it better(100% perfect).
To make it better
=========================
  After a long time to optimize my program with delay estimation, thread processing, echo path and AECM algorithm parameter etc. AECM or APM still not perfect on android. I still cannot get it work 100% perfect in a realtime VoIP call. There's some main problems:
  1. The delay of high level audio API of android cannot be estimated accurately, especially AudioRecord. So now I'm considering using low level API like OpenSLES.
  2. The core echo canceller of WebRTC on mobile is just a suppressor and in fact its not good enough. When there are people talk around, I always got a strong feedback, that's really bad. I'll pay close attention to Google, especially AECM(https://code.google.com/p/webrtc/issues/list?can=2&q=aecm&colspec=ID+Pri+Mstone+ReleaseBlock+Area+Status+Owner+Summary&x=mstone&y=owner&cells=tiles). If there's any optimization, I'll update it to this API. 

TODO List
=========================
  1. Provide a VoIP demo to show how to use this API instead of doing AECM on PCM files.
