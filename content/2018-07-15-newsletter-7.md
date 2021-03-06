+++
title = "The Embedded Working Group Newsletter - 7"
date = 2018-07-15
draft = false
in_search_index = true
template = "page.html"
aliases = ["2018-07-15/"]
+++

This is the seventh newsletter of the [Embedded WG] where we highlight new progress, celebrate cool projects, thank the community, and advertise projects that need help!

<!-- more -->

If you want to mention something in [the next newsletter], make sure to leave a comment on the issue.

[the next newsletter]: https://github.com/rust-lang-nursery/embedded-wg/issues/121
[Embedded WG]: https://github.com/rust-lang-nursery/embedded-wg

## Highlights

* We have launched the [Embedded WG Twitter]! We'll be publishing things like our newsletter here, so go ahead and follow to stay up to date. If you have something you're working on and want to share, feel free to @ us so we can retweet it!
* Work started on [porting] MUSL's `libm` (for math functions like `sin`, `cos`, etc.) has started, and already has [26 of 32 functions] ported! This crate will hopefully be included in the `core` of Rust, so it can be used by `no_std` targets such as embedded or wasm.
* The Atomic\*.{load,store} API is [now available] for the thumbv6m and msp430 targets.

[Embedded WG Twitter]: https://twitter.com/rustembedded
[26 of 32 functions]: https://github.com/japaric/libm/issues?q=is%3Aopen+is%3Aissue+milestone%3Awasm
[porting]: https://github.com/japaric/libm
[now available]: https://github.com/rust-lang/rust/pull/51953

## Embedded Projects

If you have an embedded project or blog post you would like to have featured in the Embedded WG Newsletter, make sure to mention it on the tracking issue for [the next newsletter], we would love to show it off!

* This week we have two Multirotor Flight Controller projects starting in Rust! They are both based on the [stm32f3] family of chips from STMicro.
    * [Emil Fresk] posted [on Twitter] about his project [TrustFlight], which is an open source, Rust based software library for controlling the [TrustFlight HW] he designed.
    * [Josh Mcguigan] announced in his [Blog Post] that he is planning to develop a firmware package for the [BetaFPV F3], which is an off the shelf flight controller
* We also have two projects aiming to make use of Rust on the Raspberry Pi a little easier:
    * [Adam Gausmann] shared his [Rustberry] project [on Reddit], which includes register maps and an I/O library for the Raspberry Pi
    * [Rahul Thakoor] shared his [rust_gpiozero] crate [on Medium], which is based on the Python library of similar name. He has also started writing [a series of tutorials] for developers new to working with physical hardware.


[stm32f3]: https://github.com/japaric/stm32f30x-hal
[Emil Fresk]: https://github.com/korken89
[on Twitter]: https://twitter.com/korken89/status/1016975023930830848
[TrustFlight]: https://github.com/korken89/trustflight_firmware
[TrustFlight HW]: https://github.com/korken89/trustflight_hardware
[Josh Mcguigan]: https://github.com/JoshMcguigan
[Blog Post]: https://www.joshmcguigan.com/blog/betafpv-drone-flight-controller-hello-rust/
[BetaFPV F3]: https://betafpv.com/products/beta75-bnf-tiny-whoop-quadcopter

[Adam Gausmann]: https://gitlab.com/AGausmann
[Rustberry]: https://gitlab.com/AGausmann/rustberry
[on Reddit]: https://www.reddit.com/r/rust/comments/8x1ayd/calling_all_raspberry_pi_owners_rustberry_010_has/
[Rahul Thakoor]: https://github.com/rahul-thakoor
[rust_gpiozero]: https://github.com/rahul-thakoor/rust_gpiozero
[on Medium]: https://medium.com/@rahulthakoor/physical-computing-with-rust-on-raspberry-pi-a7b6f34261a6
[a series of tutorials]: https://rahul-thakoor.github.io/physical-computing-rust/

### `embedded-hal` Ecosystem Crates

As part of the [Weekly Driver Initiative], crates that are part of the `embedded-hal` ecosystem are now tracked in the [Awesome Embedded Rust] repository. Here is a current snapshot of what is available there:

| Type                      | Status    | Count | Diff |
| :---                      | :-----    | :---- | :--- |
| [Device Crates]           | released  | 14    | 0    |
| [HAL Impl Crates]         | released  | 11    | 0    |
| [Board Support Crates]    | released  | 6     | 0    |
| [Driver Crates Released]  | released  | 9     | 0    |
| [Driver Crates WIP]       | WIP       | 30    | 0    |

[Awesome Embedded Rust]: https://github.com/rust-embedded/awesome-embedded-rust
[Weekly Driver Initiative]: https://github.com/rust-lang-nursery/embedded-wg/issues/39
[Device Crates]: https://github.com/rust-embedded/awesome-embedded-rust#device-crates
[HAL Impl Crates]: https://github.com/rust-embedded/awesome-embedded-rust#hal-implementation-crates
[Board Support Crates]: https://github.com/rust-embedded/awesome-embedded-rust#board-support-crates
[Driver Crates Released]: https://github.com/rust-embedded/awesome-embedded-rust#driver-crates
[Driver Crates WIP]: https://github.com/rust-embedded/awesome-embedded-rust#wip

## Help Wanted

* Help contribute to development of [Rust's libm] to get math functions built in to `core` for `no_std` targets!

[Rust's libm]: https://github.com/japaric/libm
