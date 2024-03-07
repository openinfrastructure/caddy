Caddy Releases
===

This repository hosts custom builds of Caddy from [https://caddyserver.com/].
See the releases section.

Install `xcaddy`:

```bash
go install github.com/caddyserver/xcaddy/cmd/xcaddy@latest
```

Use the build script to build a custom version.

Note the ratelimit extension assumes no moving gc and may throw the following
error if included in recent versions of go:

```
panic: Something in this program imports go4.org/unsafe/assume-no-moving-gc to declare that it assumes a non-moving garbage collector, but your version of go4.org/unsafe/assume-no-moving-gc hasn't been updated to assert that it's safe against the go1.19 runtime. If you want to risk it, run with environment variable ASSUME_NO_MOVING_GC_UNSAFE_RISK_IT_WITH=go1.19 set. Notably, if go1.19 adds a moving garbage collector, this program is unsafe to use.

goroutine 1 [running]:
go4.org/unsafe/assume-no-moving-gc.init.0()
	go4.org/unsafe/assume-no-moving-gc@v0.0.0-20211027215541-db492cf91b37/untested.go:25 +0x1f4
```
