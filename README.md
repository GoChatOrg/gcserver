
# GoChat Server - A Secure Text Chat Server

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

This Go-based messaging system implements a secure TCP server-client communication protocol. The server and clients use elliptic curve Diffie-Hellman (ECDH) key exchange to establish a shared secret for encrypted message exchanges, providing secure, authenticated communication.

## Features

1. **ECDH Key Exchange:** The server and client exchange public keys to establish a shared secret.
2. **AES Encryption:** Messages are encrypted using AES.
3. **IPv4 and IPv6 Support:** The server now supports binding to both IPv4 and IPv6 Tailscale addresses, based on user preferences.
4. **Basic Commands:** Support for user registration, listing active users, sending messages, and fetching server information.
5. **Operator Commands:** Support for basic server operator command including banning and unbanning of clients.

## Requirements

1. [Go](https://golang.org/doc/install) (version 1.24.0 or later)

## Installation

Clone the repository and navigate to the project directory:

```sh
git clone https://github.com/GoChatOrg/gcserver.git
cd gcserver
```

## Building the Server

To build the server, run the following command:

```sh
go build
```

## Running the Server

The server will automatically listen for incoming client connections on port 12345 by default, and will listen on the localhost interface. To change this, copy the `.env.example` file to `.env` and edit the required values.

1. Ensure networking is active and configured.
2. (Optional) Ensure your `.env` file is configured correctly.
3. Start the server with:

   ```sh
   go run .
   ```
   
   If you did not configure your `.env` file, the server will default to IPv4 mode. To enable IPv6 or dual-stack mode, configure the `IPV4` and/or `IPV6` flags in your `.env` file.

   - If no flags are provided, the server defaults to IPv4 mode.

4. The server will display its IP address(es) and listen for incoming client connections.

### Server Commands

The server supports the following commands sent from clients:

- `REGISTER <ClientID>`: Registers a new client with a unique ID.
- `SEND <RecipientID|ALL> <Message>`: Sends a message to a specific client or broadcasts to all.
- `LIST`: Lists all connected clients.
- `SERVERHELP`: Lists available server commands.

#### Operator Commands

- `SERVERINFO`: Displays server information.
- `KICK <ClientID>`: Disconnects the specified client from the server.
- `BAN <ClientID>`: Bans the specified client and disconnects them if connected.
- `UNBAN <ClientID>`: Removes a client from the banned list.
- `LISTBANS`: Lists all banned clients.

## Running the Client

**UPDATE:** Please refer to the [GoChat Client](https://github.com/GoChatOrg/gcclient) for usage instructions.

## Example Usage

1. Start the server:

   ```sh
   go run .
   ```
   
   This starts the server in IPv4 mode, binding to the localhost interface on port 12345.

## Notes

- Each client should register with a unique identifier (the server will reject duplicate identifiers).
- Both the client and server are cross-platform and have been tested on macOS, Windows, Linux, and FreeBSD.
- The server can now operate in IPv4, IPv6, or both modes, depending on the specified flags.

## Security Considerations

- Messages are encrypted with AES.
- Shared secrets are derived using ECDH and hashed with SHA-256.
- Operator commands are restricted to the client initially registered as the operator.

## Contributing

Please refer to our [CONTRIBUTING.md](docs/CONTRIBUTING.md) file for details on how to contribute to this project.

## Also See

- [gcclient](https://github.com/tailsecurity/padclient) for the official Padserve Client implementation

## License

This project is licensed under the MIT license.
