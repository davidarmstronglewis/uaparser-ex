# NIF for Elixir.UAParserRS

## To build the NIF module:

- Your NIF will now build along with your project.

## To load the NIF:

```elixir
defmodule UAParserRS do
    use Rustler, otp_app: :uaparser, crate: "uaparser"

    # When your NIF is loaded, it will override this function.
    def add(_a, _b), do: :erlang.nif_error(:nif_not_loaded)
end
```

## Examples

[This](https://github.com/hansihe/NifIo) is a complete example of a NIF written in Rust.
