# -------- Stage 1: Build the Go binary --------
FROM golang:1.22.5 AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy go.mod and go.sum first to leverage Docker cache
COPY go.mod ./

# Download dependencies
RUN go mod download

# Copy the entire source code
COPY . .

# Build the Go binary statically for Linux
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o main .

# -------- Stage 2: Create a minimal runtime image --------
FROM gcr.io/distroless/static

WORKDIR /

# Copy the binary from the builder stage
COPY --from=builder /app/main .

# Optional: Copy static files if your app serves assets
COPY --from=builder /app/static /static

# Expose the app port
EXPOSE 8080

# Run the app
CMD ["./main"]
