# QueryApiImpl

```c
HRESULT WINAPI QueryApiImpl(
    const GUID *classId,
    REFIID interfaceId,
    void **out
);
```

`classId` indicates one of the [COM classes](COM/README.md) provided by the runtime, on success `out` contains a pointer to the requested interface.
If the provided `classId` is not provided by the runtime `QueryApiImpl` returns `0x80070032` (ERROR_NOT_SUPPORTED as HRESULT).
