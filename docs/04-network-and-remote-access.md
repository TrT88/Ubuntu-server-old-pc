# Network and Remote Access

## Network hardware

The system was configured with:

- Onboard Ethernet.
- A USB Wi-Fi adapter based on the Realtek RTL8710BU chipset.
- Linux driver: `rtl8xxxu`.

## Network priority

The configured route metrics were:

| Connection | Metric |
|---|---:|
| Ethernet | 100 |
| Wi-Fi | 600 |

A lower metric gives Ethernet priority when both routes are available.

## Inspect network configuration

Run on Ubuntu:

    ip -br addr
    ip route
    ip route get 1.1.1.1
    nmcli device status

## Remote access with SSH

SSH was tested successfully from a Mac to the physical Ubuntu Server.

Generic example:

    ssh serveruser@100.100.100.22

Replace the example username and address with the actual values in your own environment.

## Tailscale

Tailscale was configured to provide private remote connectivity between devices.

Do not publish real device names, account details, authentication keys or tailnet IP addresses.

## Privacy

Before sharing diagnostic output, remove:

- Usernames and hostnames.
- Public and private IP addresses.
- Wi-Fi SSIDs and passwords.
- Tailscale device and account details.
- Authentication keys and tokens.
