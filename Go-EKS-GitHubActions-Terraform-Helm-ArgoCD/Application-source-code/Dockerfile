FROM golang:1.19
# Set destination for COPY
WORKDIR /app
# Download Go modules
COPY go.mod go.sum ./
RUN go mod download
# Copy the source code. Note the slash at the end
COPY . .
RUN go build -o main .
EXPOSE 8080
CMD ["./main"]
