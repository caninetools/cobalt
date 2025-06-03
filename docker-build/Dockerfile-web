FROM alpine:latest AS builder
WORKDIR /app

# Set env here for build
ENV WEB_HOST="cobalt.canine.tools"
ENV WEB_DEFAULT_API="https://cobalt-backend.canine.tools/"
ENV WEB_PLAUSIBLE_HOST="plausible.canine.tools"

RUN apk add --no-cache nodejs npm git
RUN npm install -g pnpm

# Copy build stuff
COPY pnpm-workspace.yaml /app/
COPY web/ /app/web/
COPY packages/ /app/packages/
COPY .git /app/.git

# Build frontend
WORKDIR /app/web
RUN pnpm install
RUN pnpm run build

FROM caddy:alpine AS final
WORKDIR /srv
COPY --from=builder /app/web/build /srv
COPY docker-build/Caddyfile /etc/caddy/Caddyfile

EXPOSE 80