**MHDDOS_2.5.py** is a powerful multi-handler DDoS (Distributed Denial of Service) attack tool designed for educational and testing purposes. This tool allows users to perform various types of DDoS attacks using multiple methods, including Layer 4 and Layer 7 attacks. It is equipped with the capability to utilize Tor for anonymity, making it a versatile option for penetration testers and cybersecurity enthusiasts.

The tool supports a range of attack methods, including HTTP GET and POST requests, as well as amplification attacks using protocols like NTP and DNS. It also allows for the use of proxy servers to obfuscate the attacker's IP address, enhancing the stealth of the operation.

### Key Features
- **Multi-Method Support:** Offers various attack methods, including Layer 4 and Layer 7 techniques.
- **Tor Integration:** Allows the use of Tor to anonymize the attacker's IP address.
- **Proxy Support:** Enables the use of proxy servers to further conceal the attacker's identity.
- **Real-Time Monitoring:** Displays the number of requests sent during the attack in real-time.
- **Customizable Parameters:** Users can specify target URLs, number of threads, duration of the attack, and proxy settings.

## Requirements
- Python 3.x
- Tor installed and configured on the system
- Required Python libraries (e.g., `requests`, `socket`, `subprocess`, `threading`, etc.)

## Usage
To run the tool, use the following command structure:

```bash
python3 MHDDOS_2.5.py <method> <target_url> <proxy_type> <threads> <proxy_file> <rpc> <duration>
```

### Parameters
- `<method>`: The attack method to be used (e.g., `GET`, `POST`, `SYN`, etc.).
- `<target_url>`: The URL or IP address of the target to be attacked.
- `<proxy_type>`: The type of proxy to be used (e.g., `0` for all proxies, `1` for HTTP, `4` for SOCKS4, `5` for SOCKS5).
- `<threads>`: The number of threads to be used for the attack.
- `<proxy_file>`: The path to the file containing the list of proxies.
- `<rpc>`: The number of requests to be sent per connection.
- `<duration>`: The duration of the attack in seconds.

### Example Command
```bash
python3 MHDDOS_2.5.py GET http://example.com 1 100 proxies.txt 10 60
```
This command will initiate a GET request attack on `http://example.com` using 100 threads for 60 seconds, utilizing proxies listed in `proxies.txt`.

## Attack Methods
### Layer 4 Methods
- **TCP**: Basic TCP connection flood.
- **UDP**: User Datagram Protocol flood.
- **SYN**: SYN flood attack.
- **ICMP**: Internet Control Message Protocol flood.

### Layer 7 Methods
- **GET**: HTTP GET request flood.
- **POST**: HTTP POST request flood.
- **CFB**: Custom flood method.
- **DGB**: DDoS Guard Bypass method.

## Real-Time Monitoring
The tool includes a real-time monitoring feature that displays the number of requests sent during the attack. This information is updated every second and can be viewed in the console output.

## Important Notes
- **Ethical Use**: This tool is intended for educational purposes and should only be used in controlled environments with permission from the target.
- **Legal Compliance**: Ensure compliance with local laws and regulations regarding DDoS attacks and cybersecurity practices.

## Conclusion
**MHDDOS_2.5.py** is a comprehensive tool for simulating DDoS attacks, providing users with the ability to test their systems' resilience against such threats. With its multi-method support and integration with Tor and proxies, it serves as a valuable resource for cybersecurity professionals and enthusiasts alike. Always remember to use this tool responsibly and ethically.
