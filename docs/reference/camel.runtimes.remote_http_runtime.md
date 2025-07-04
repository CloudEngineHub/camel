<a id="camel.runtimes.remote_http_runtime"></a>

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime"></a>

## RemoteHttpRuntime

```python
class RemoteHttpRuntime(BaseRuntime):
```

A runtime that runs functions in a remote HTTP server.
You need to run the API server in the remote server first.

**Parameters:**

- **host** (str): The host of the remote server.
- **port** (int): The port of the remote server. (default: :obj:`8000`) (default: 8000)
- **python_exec** (str): The python executable to run the API server. (default: :obj:`python3`)

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.__init__"></a>

### __init__

```python
def __init__(
    self,
    host: str,
    port: int = 8000,
    python_exec: str = 'python3'
):
```

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.build"></a>

### build

```python
def build(self):
```

**Returns:**

  RemoteHttpRuntime: The current runtime.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime._cleanup"></a>

### _cleanup

```python
def _cleanup(self):
```

Clean up the API server when exiting.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.add"></a>

### add

```python
def add(
    self,
    funcs: Union[FunctionTool, List[FunctionTool]],
    entrypoint: str,
    redirect_stdout: bool = False,
    arguments: Optional[Dict[str, Any]] = None
):
```

Add a function or list of functions to the runtime.

**Parameters:**

- **funcs** (Union[FunctionTool, List[FunctionTool]]): The function or list of functions to add.
- **entrypoint** (str): The entrypoint for the function.
- **redirect_stdout** (bool): Whether to return the stdout of the function. (default: :obj:`False`)
- **arguments** (Optional[Dict[str, Any]]): The arguments for the function. (default: :obj:`None`)

**Returns:**

  RemoteHttpRuntime: The current runtime.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.ok"></a>

### ok

```python
def ok(self):
```

**Returns:**

  bool: Whether the API Server is running.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.wait"></a>

### wait

```python
def wait(self, timeout: int = 10):
```

Wait for the API Server to be ready.

**Parameters:**

- **timeout** (int): The number of seconds to wait. (default: :obj:`10`) (default: 10)

**Returns:**

  bool: Whether the API Server is ready.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.__del__"></a>

### __del__

```python
def __del__(self):
```

Clean up the API server when the object is deleted.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.stop"></a>

### stop

```python
def stop(self):
```

**Returns:**

  RemoteHttpRuntime: The current runtime.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.reset"></a>

### reset

```python
def reset(self):
```

**Returns:**

  RemoteHttpRuntime: The current runtime.

<a id="camel.runtimes.remote_http_runtime.RemoteHttpRuntime.docs"></a>

### docs

```python
def docs(self):
```

**Returns:**

  str: The URL for the API documentation.
