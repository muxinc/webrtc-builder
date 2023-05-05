# Webrtc-builder

This is ultimately a fork of:
https://github.com/webrtc-sdk/webrtc-build

This builds the actual libwebrtc binaries in Github Actions which are then picked up in other repos for distribution.

To create a new build (for a new version of libwebrtc) update build/VERSION with the appropriate values.

After committing the changes tag the release with something appropriate to the build like:
```
git tag -a m104.5112.09 -m "m104.5112.09"
git push origin --tags
```

Wait for it to build (a while). Today the build uses dangerously large amounts of storage (a far more pressing problem than CPU), and it may be a good idea to evaluate other options for the runners.

To actual push the build to artifactory and then consume it please see: https://github.com/muxinc/webrtc-android

If you were adventurous there's quite a lot of scope to clean up the above.