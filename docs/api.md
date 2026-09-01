# API Reference

[简体中文](api.zh-CN.md) | [Docs Index](README.md)

This inventory is generated from `go doc -short` for the packages in this repository. It is a quick public-surface map; source files and tests remain the authority for exact semantics.

## Packages

### `gnalloy.org/observability`

Package name: `observability`

```text
var ErrInvalidExporter = errors.New("gnalloy/observability: invalid exporter")
func ExportSnapshot(w io.Writer, snapshotter Snapshotter, exporter Exporter) error
type AtomicChannelRecorder struct{ ... }
    func NewAtomicChannelRecorder() *AtomicChannelRecorder
type ChannelLatencyRecorder interface{ ... }
type ChannelMetrics struct{ ... }
type ChannelRecorder interface{ ... }
    func NormalizeChannelRecorder(recorder ChannelRecorder) ChannelRecorder
type Exporter interface{ ... }
type MessageSizer interface{ ... }
    var ReadableBytesSizer MessageSizer = MessageSizerFunc(func(msg any) int64 { ... })
    func NormalizeMessageSizer(sizer MessageSizer) MessageSizer
type MessageSizerFunc func(msg any) int64
type NoopChannelRecorder struct{}
type PrometheusConfig struct{ ... }
type PrometheusExporter struct{ ... }
    func NewPrometheusExporter(cfg PrometheusConfig) *PrometheusExporter
type Snapshotter interface{ ... }
```
