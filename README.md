# UdpClientServer

Simple client server using UDP (erlang's :gen_udp library) in elixir
This leverages the [elixir-socket](https://github.com/meh/elixir-socket), which in turn is a wrapper around `get_tcp`, `gen_udp`, `gen_tscp` and `ssl` from erlang.

## Installation

Simply clone this repo, then run `mix deps.get` to fetch all the dependencies


## Playing with the repo


The code is in [lib/udp_client_server.ex](lib/udp_client_server.ex).
Currently, this doesn't run anything by default. To run it, I suggest opening 2 iex shells (iex is the elixir REPL), loading up the context of the repo.


### Window 1: server
```
iex -S mix
Erlang/OTP 20 [erts-9.0] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

Interactive Elixir (1.4.5) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> UdpClientServer.launch_server
```


### Window 2: client
```
iex -S mix
Erlang/OTP 20 [erts-9.0] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

Compiling 1 file (.ex)
Interactive Elixir (1.4.5) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> UdpClientServer.send_data("hello")
:ok
```
