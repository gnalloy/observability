# API 参考

[English](api.md) | [文档索引](README.zh-CN.md)

本清单由本仓库 package 的 `go doc -short` 生成，用于快速查看公共面。精确语义以源码和测试为准。

## 包

### `gnalloy.org/observability`

包名：`observability`

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
