# Traefik 101

## Overview

Traefik adalah Edge Router open-source yang memberikan pengalaman atau experience dalam publishing service-service milik kita menjadi mudah dan menyenangkan!

Traefik menerima requests atas nama sistem milik kita dan mencari tahu komponen mana yang bertanggung jawab untuk menanganinya.

Apa yang membedakan Traefik adalah, selain memiliki banyak fitur, Traefik dapat secara otomatis menemukan konfigurasi yang tepat untuk service kita (Auto Service Discovery).

Traefik secara native sesuai dengan mayoritas teknologi cluster yang ada saat ini, seperti Kubernetes, Docker, Docker Swarm, AWS, Mesos, Marathon, dan banyak lagi; dan dapat menangani semua dalam waktu yang bersamaan.

## Concepts

(Replace this text with Concepts intro)

### Entrypoints

(Replace this text with Entrypoints concept text)

### Frontends

(Replace this text with Frontends concept text)

### Backends

(Replace this text with Backends concept text)

## Configuration

(Replace this text with Configuration intro)

### Static Configuration

(Replace this text with Static Configuration text)

```toml
################################################################
# Global configuration
################################################################

# Enable debug mode
#
# Optional
# Default: false
#
# debug = true

# Log level
#
# Optional
# Default: "ERROR"
#
# logLevel = "DEBUG"

# Entrypoints to be used by frontends that do not specify any entrypoint.
# Each frontend can specify its own entrypoints.
#
# Optional
# Default: ["http"]
#
# defaultEntryPoints = ["http", "https"]

################################################################
# Entrypoints configuration
################################################################

# Entrypoints definition
#
# Optional
# Default:
[entryPoints]
    [entryPoints.http]
    address = ":80"

################################################################
# Traefik logs configuration
################################################################

# Traefik logs
# Enabled by default and log to stdout
#
# Optional
#
# [traefikLog]

# Sets the filepath for the traefik log. If not specified, stdout will be used.
# Intermediate directories are created if necessary.
#
# Optional
# Default: os.Stdout
#
# filePath = "log/traefik.log"

# Format is either "json" or "common".
#
# Optional
# Default: "common"
#
# format = "common"

################################################################
# Access logs configuration
################################################################

# Enable access logs
# By default it will write to stdout and produce logs in the textual
# Common Log Format (CLF), extended with additional fields.
#
# Optional
#
# [accessLog]

# Sets the file path for the access log. If not specified, stdout will be used.
# Intermediate directories are created if necessary.
#
# Optional
# Default: os.Stdout
#
# filePath = "/path/to/log/log.txt"

# Format is either "json" or "common".
#
# Optional
# Default: "common"
#
# format = "common"

################################################################
# API and dashboard configuration
################################################################

# Enable API and dashboard
[api]

  # Name of the related entry point
  #
  # Optional
  # Default: "traefik"
  #
  # entryPoint = "traefik"

  # Enabled Dashboard
  #
  # Optional
  # Default: true
  #
  # dashboard = false

################################################################
# Ping configuration
################################################################

# Enable ping
[ping]

  # Name of the related entry point
  #
  # Optional
  # Default: "traefik"
  #
  # entryPoint = "traefik"

################################################################
# Docker configuration backend
################################################################

# Enable Docker configuration backend
[docker]

# Docker server endpoint. Can be a tcp or a unix socket endpoint.
#
# Required
# Default: "unix:///var/run/docker.sock"
#
# endpoint = "tcp://10.10.10.10:2375"

# Default domain used.
# Can be overridden by setting the "traefik.domain" label on a container.
#
# Optional
# Default: ""
#
# domain = "docker.localhost"

# Expose containers by default in traefik
#
# Optional
# Default: true
#
# exposedByDefault = true
```

### Dynamic Configuration

(Replace this text with Dynamic Configuration text)
