FROM golang
# Set destination for COPY
WORKDIR /app
COPY dispatcher.go ./
COPY static ./
RUN go build dispatcher.go
# Enable usage of this port
EXPOSE 80

# Run code
CMD ["./dispatcher"]

# Build it with : docker build -t "web:Dockerfile" .