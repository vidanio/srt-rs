# srt-rs

[![Build Status](https://travis-ci.org/russelltg/srt-rs.svg?branch=master)](https://travis-ci.org/russelltg/srt-rs) [![Build status](https://ci.appveyor.com/api/projects/status/q0eu7a4mtunff041?svg=true)](https://ci.appveyor.com/project/GuapoTaco/srt-rs)

> NOTE: THIS IS NOT PRODUCTION READY.

Pure rust implementation of SRT (Secure Reliable Transport)

Reference implementation is available at https://github.com/haivision/srt

# Features

- Fast (heap allocations are rare)
- Single-threaded

# What works

- [x] Listen server connecting
- [x] Client (connect) connecting
- [ ] Rendezvous connecting
- [x] Receiving
- [x] Sending
- [ ] Special SRT packets
- [ ] Actual SRT (TSBPD)


# Heap efficiency

Running under massif, the maximum memory usage is around 6KB for transmitting video. for srt-rs.

For the reference implementation, this number grows to 1.2MB, so around a 2X difference. 
