# `spin + python + uv`

Package and run python projects into WASM components. Spin is a framework for running event-driven microservice applications with WebAssembly (Wasm) components. Python project and dependencies are managed with `uv`.

## Quickstart

```
spin up --build
```

## Example
<table>
<tr>
<td> Build & Run </td> <td> Test </td>
</tr>
<tr>
<td>

```Shell
$ spin up --build
Building component hello-world with `uv run --no-editable \
    componentize-py -w spin-http componentize spin_py_demo -o main.wasm`
Using CPython 3.13.5 interpreter at: /usr/bin/python3
Creating virtual environment at: .venv
Installed 3 packages in 17ms
Component built successfully
Finished building all Spin components
Logging component stdio to ".spin/logs/"
Preparing Wasm modules is taking a few seconds...

Serving http://127.0.0.1:3000
Available Routes:
  hello-world: http://127.0.0.1:3000 (wildcard)
```
</td>
<td>
    
```Shell
$ curl http://127.0.0.1:3000
Hello from Python!
```
</td>
</tr>
</table>


## References

* https://spinframework.dev/v3/python-components
* https://spinframework.dev/
* https://docs.astral.sh/uv/
