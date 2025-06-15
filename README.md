# Traffic Limiter

Traffic Limiter is a free, open-source GTK application that lets you easily set traffic control (TC) bandwidth limits on your network interfaces. The program uses the Linux `tc` command and a graphical interface to apply upload and download limits with Token Bucket Filter (TBF) rules.

## Features

- List available network interfaces and their IP addresses.
- Easily set upload and download limits (in kbps).
- Applies TC rules for both egress (upload) and ingress (download) using an `ifb0` virtual interface.
- Clear applied limits with a single click.
- Packaged for Debian-based systems.

## Installation
A Debian package (.deb) is provided for easy installation on Debian-based systems.

Install the Package:
    sudo dpkg -i traffic-limiter_1.0.deb
You can now launch Traffic Limiter either by running:
    traffic-limiter
or from your desktop application menu (if a desktop file was installed).

### USAGE

    Select an Interface: The application displays all network interfaces and their IP addresses. Select the desired interface from the list.

    Set Bandwidth Limits: Enter numeric values (in kbps) for both upload and download limits.

    Apply Limits: Click the "Apply Limit" button. The program will automatically create the necessary TC rules to enforce your settings.

    Clear Limits: Click the "Clear Limit" button to remove any active limits.

#### From Source

1. **Clone the Repository:**


   git clone https://github.com/yourusername/traffic-limiter.git
   cd traffic-limiter

##### From Source

Traffic Limiter is licensed under the GNU General Public License v3 (GPLv3). See the LICENSE file for the full license text.
