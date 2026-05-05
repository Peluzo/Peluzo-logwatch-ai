# Stub image for Step 1 — replaced when Laravel is added.
FROM alpine:3.20
RUN apk add --no-cache curl
EXPOSE 8000
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
    CMD curl -fsS http://127.0.0.1:8000/health || exit 1
CMD ["sh", "-c", "echo OK > /tmp/health && busybox httpd -f -p 8000 -h /tmp"]
