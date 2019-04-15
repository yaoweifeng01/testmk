<h1>Python API Reference</h1>

!!! important
		CyberRT API for Python. For the source please switch to the 
    [CyberRT for Python](https://github.com/ApolloAuto/apollo/tree/master/cyber/python).

## `cyber`

- `init(module_name="cyber_py")`
- `ok()`
- `shutdown()`
- `is_shutdown()`
- `waitforshutdown()`

## `cyber.Node`

- `__init__(name):`
- `register_message`
- `create_writer(name, data_type, qos_depth=1)`
- `reader_callback(name)`
- `create_reader(name, data_type, callback, args=None)`
- `create_client(name, request_data_type, response_data_type)`
- `service_callback(name)`
- `create_service(name, req_data_type, res_data_type, callback, args=None)`
- `spin()`

## `cyber.Recorder.RecordReader`

- `__init__(file_name)`
- `__del__`
- `read_messages(start_time=0, end_time=18446744073709551615)`
- `get_messagenumber(channel_name)`
- `get_protodesc(channel_name)`
- `get_headerstring()`
- `reset()`
- `get_channellist()`

## `cyber.Recorder.RecordWriter`

- `__init__(file_segmentation_size_kb=0,
                 file_segmentation_interval_sec=0)`
- `__del__()`
- `open(path)`
- `close()`
- `write_channel(channel_name, type_name, proto_desc)`
- `write_message(channel_name, data, time, raw=True)`
- `set_size_fileseg(size_kilobytes)`
- `set_intervaltime_fileseg(time_sec)`
- `get_messagenumber(channel_name)`
- `get_messagetype(channel_name)`
- `get_protodesc(channel_name)`

## `cyber.cyber_time.Duration`

- `__init__(other)`
- `__del__()`
- `sleep()`
- `__str__()`
- `to_sec()`
- `to_nsec()`
- `iszero()`
- `__add_(other)`
- `__radd__(other)`
- `__sub__(other)`
- `__lt__(other)`
- `__gt__(other)`
- `__le__(other)`
- `__ge__(other)`
- `__eq__(other)`
- `__ne__(other)`

## `cyber.cyber_time.Time`

- `__init__(other)`
- `__del__()`
- `__str__()`
- `iszero()`
- `now()`
- `mono_time()`
- `to_sec()`
- `to_nsec()`
- `sleep_until()`
- `__add_()`
- `__radd__()`
- `__sub__()`
- `__lt__()`
- `__gt__()`
- `__le__()`
- `__ge__()`
- `__eq__()`
- `__ne__()`

## `cyber.cyber_time.Rate`

- `__init__(other)`
- `__del__()`
- `__str__()`
- `iszero()`
- `sleep()`
- `reset()`
- `get_cycle_time()`
- `get_expected_cycle_time()`

