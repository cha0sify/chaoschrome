# ChaosChrome (CChrome)
Snapdragon-optimized Browser based on CAF-chrome4sdp (https://www.codeaurora.org/cgit/quic/chrome4sdp/)

to build this package, look at CAF-Wiki  to sync and build  successfully (https://www.codeaurora.org/xwiki/bin/Chromium+for+Snapdragon/Build & https://www.codeaurora.org/xwiki/bin/Chromium+for+Snapdragon/m42_build_instructions)
if your Environment Setup is complete, use this .gclient-file to build CChrome_m42 instead of swe_m42: 

solutions = [
  { "name"        : "src",
    "url"         : "git://codeaurora.org/quic/chrome4sdp/chromium/src.git@refs/remotes/origin/m42",
    "deps_file"   : "DEPS",
    "managed"     : True,
    "safesync_url": "",
"custom_deps" : {
      "src/swe/browser" : "https://github.com/ChaOSChriS/chaoschrome.git@refs/remotes/origin/m42"
    }
  },
]
target_os = ["android"]

