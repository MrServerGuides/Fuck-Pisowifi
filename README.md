Here's a `README.md` based on your Python script:

---

# Advanced HTTP Attack Script

This Python script simulates high-load HTTP requests to a target WiFi router or server. It's designed to cause disruptions on vulnerable WiFi connections, particularly those using localhost-dependent gateways, like Pisowifi. The script demonstrates a potential attack vector known as HTTP request smuggling.

**Important**: This tool is meant for educational purposes only. Use it only on networks where you have explicit consent. Unauthorized use could be illegal and harmful.

---

## Features

- Simulates high-load HTTP requests using a crafted attack (HTTP request smuggling).
- Supports both HTTP and HTTPS protocols (with SSL).
- Allows customization of attack parameters such as the number of requests, target IP, and port.
- Uses multi-threading to send requests simultaneously, enhancing the attack's effectiveness.
- Progress bar for tracking attack progress.
- Detailed status updates with real-time feedback on request success/failure.

---

## Requirements

Before running the script, ensure you have the following installed:

- Python 3.x
- Required Python libraries:
  - `tqdm`: For displaying a progress bar during execution.
  - `colorama`: For colorful console output.
  - `rich`: For rich text and progress bar handling.
  
Install the dependencies using pip:
```bash
pip install tqdm colorama rich
```

---

## Usage

1. Clone the repository or download the script file.
2. Run the script in your terminal:
    ```bash
    python3 attack_script.py
    ```

3. Input the following when prompted:
    - **Target WiFi Router Gateway URL** (e.g., `192.168.1.1`)
    - **Target Port** (Default: `80`)
    - **Total Request Limit** (The number of requests you wish to send)

The script will start simulating requests and display progress in the terminal.

---

## How it Works

1. **Initial Setup**:
    - The script prompts for the target router's URL and port.
    - It resolves the router's hostname to an IP address.
    - It validates the URL and port input before continuing.

2. **Attack Process**:
    - The script uses multi-threading to generate and send multiple HTTP requests.
    - The requests are crafted with HTTP request smuggling techniques (e.g., chunked transfer encoding and header manipulation).
    - If an error occurs (e.g., connection failure), the script automatically restarts the attack threads.

3. **Attack Termination**:
    - After the attack completes, the script prints a summary of the successful requests and any errors encountered.

---

## Disclaimer

This script simulates an HTTP attack and may cause disruptions to vulnerable networks. **Use responsibly** and **only with permission**. The author takes no responsibility for the misuse of this tool.

- **Author**: Cyber Unice / Xyrax / Kyla / Psuedo

---

## Credits

This script was developed and contributed by **Cyber Unice**, **Xyrax**, **Kyla**, and **Psuedo**. We acknowledge the importance of ethical hacking and the responsible use of cybersecurity tools.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

