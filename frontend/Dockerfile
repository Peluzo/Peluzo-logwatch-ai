# Stub image for Step 1 — replaced when React dev server / static build is added.
FROM alpine:3.20
RUN apk add --no-cache curl
EXPOSE 3000
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
    CMD curl -fsS http://127.0.0.1:3000/ || exit 1
CMD ["sh", "-c", "echo '<html><body>frontend stub</body></html>' > /tmp/index.html && busybox httpd -f -p 3000 -h /tmp"]
