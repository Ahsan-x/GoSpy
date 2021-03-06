<h1 align="center">GoSpy</h1>

<p align="center">
    <img height=200 width=200 src="./icon.png"/>
    <br/>
    <a href="https://github.com/psidex/GoSpy/actions" >
        <img src="https://github.com/psidex/GoSpy/workflows/go%20build%20windows/badge.svg" />
    </a>
    <a href="https://github.com/psidex/GoSpy/actions" >
        <img src="https://github.com/psidex/GoSpy/workflows/go%20build%20ubuntu/badge.svg" />
    </a>
    <br/>
    <a href="https://goreportcard.com/report/github.com/psidex/GoSpy" >
        <img src="https://goreportcard.com/badge/github.com/psidex/GoSpy" />
    </a>
    <a href="./LICENSE" >
        <img src="https://img.shields.io/github/license/psidex/GoSpy" />
    </a>
    <a href="https://ko-fi.com/M4M18XB1" >
        <img src="https://img.shields.io/badge/support%20me-Ko--fi-orange.svg?style=flat&colorA=35383d" />
    </a>
</p>

<p align="center">A cross-platform post-exploitation tool for penetration testing</p>

## Disclaimer

This project should be used for authorized testing or educational purposes only.

It is the final user's responsibility to obey all applicable local, state, and federal laws.

Authors assume no liability and are not responsible for any misuse or damage caused by this program.

## Usage

GoSpy consists of 2 binaries, `gospy` is what you execute on your target machine and `gospyserver` is what you run on
your machine to interact with it.

## Features

These are almost all currently a WIP

- [x] Cross-platform with `CGO_ENABLED=0` (compiles to any target that Go supports)
- [x] Basic plaintext communication over TCP sockets
- [x] AES-256 encrypted communication over TCP sockets using a shared password
  - Note: This will cause a noticeable increase in response times
- [x] Safe error handling for client so it won't suddenly drop on error
- [x] Reverse shell
  - Note: This is not a full reverse shell, it is executing commands in a shell on the target and then returning their
  output, rather than streaming a full shell process
- [ ] Screen grab
- [ ] File grab
- [ ] File drop
- [ ] Execute Lua scripts on target machine (using [gopher-lua](https://github.com/yuin/gopher-lua))
- [ ] More?

## Screenshot

![](./demo.png)

## Why?

I wrote this project to learn more about both Go and penetration testing, as I recently completed an "Ethical Hacking"
unit for my university course and am interested in learning more.

## Credits

- Icon from [gopherize.me](https://gopherize.me/)
- [go-prompt](https://github.com/c-bata/go-prompt/) for the interactive prompt on the server
- [JP Bruins Slot](https://itnext.io/encrypt-data-with-a-password-in-go-b5366384e291) for most of the encryption code
