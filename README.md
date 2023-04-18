# home-assistant-otlp
Stand-alone HomeAssistant/OpenTelemetry monitoring application.

This is intended to listen to a (configurable) set of HomeAssistant events and translate those into OpenTelemetry spans. One of the primary notions is to _relate_ events via a Parent Span based on actions (if possible). Spans will be published via the usual mechanisms: this is **not** using the JVM instrumentation classes, so configuration is likely to be a mix of application configuration and OTLP "auto-configuration".

