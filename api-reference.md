# API Reference

## Base URL

Becoming a super hero is a fairly straight forward process:

```
https://api.saryno.com
```

| Version | Status | Default |
| :--- | :--- | :--- |
| 1 | Insiders Only | ✓ |

## Snowflakes

```python
EPOCH = To be added...

snowflake_id = 42388375784780768

# Keep only the last 41 bits
timestamp = snowflake_id >> 22 + EPOCH
```

