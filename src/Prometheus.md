# Prometheus
## Testing
1. Start Prometheus
```
./prometheus --config.file=prometheus.yml
```
- Notes that the scrape interval is configured to 500ms
```yaml
global:
  scrape_interval: 500ms
```
2. Run `prometheus_publisher`
```
cargo run
```
- This app reads frames from a serial port and exposes them as a webhook for Prometheus to scrape