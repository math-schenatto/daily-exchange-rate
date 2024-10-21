# Dollar Exchange Rate API

## Description

This is a simple API that provides the dollar exchange rate for the day. The project consists of a server that receives requests and a client that makes calls to the API. Each request is logged in an SQLite3 database for persistence. The project also implements timeout control on requests and logs for monitoring.

## Project Structure

- **client/**: Contains the code for the client that makes requests to the API.
- **server/**: Contains the code for the server that processes requests and persists data.
- **database/**: Contains the SQLite3 configuration and database schema.

## Requirements

- Go (version 1.21 or higher)
- SQLite3

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/math-schenatto/daily-exchange-rate.git
   cd daily-exchange-rate
   ```

2. Install the dependencies:
   ```bash
   go mod tidy
   ```

## How to Use

### Running the Server

1. Run the server initializer:
   ```bash
   go run cmd/server/main.go
   ```

### Making Requests with the Client

1. Make a request with the client:
   ```bash
   cd ../client
   ```

### Example Request

```bash
curl -X GET http://localhost:8081/cotacao
```

## Features

- **Return of the Dollar Rate**: The API provides the dollar exchange rate for the day.
- **Request Persistence**: Each request is logged in an SQLite3 database.
- **Context with Timeout**: Implementation of timeout to ensure that requests do not hang.
- **Log Registration**: Logs are generated to monitor requests and server operation.

## Contribution

Contributions are welcome! Feel free to open issues or pull requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
