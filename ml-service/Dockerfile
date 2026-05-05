# Stub image for Step 1 — replaced when Python ML app is added.
FROM alpine:3.20
RUN apk add --no-cache curl
EXPOSE 8001
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
    CMD curl -fsS http://127.0.0.1:8001/health || exit 1
CMD ["sh", "-c", "mkdir -p /tmp/ml && echo OK > /tmp/ml/health && busybox httpd -f -p 8001 -h /tmp/ml"]
