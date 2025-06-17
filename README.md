Traffic Limiter

Traffic Limiter is a free, open-source GTK application that lets you easily set traffic control (TC) bandwidth limits on your network interfaces. The program uses the Linux tc command and a graphical interface to apply upload and download limits using Token Bucket Filter (TBF) rules. It now includes support for ingress limiting via an ifb0 virtual interface.

Features

- Interface Listing: Displays available network interfaces along with their IP addresses.
- Flexible Rate Configuration: Set bandwidth limits with a choice of units (B/s, KiB/s, MiB/s). Input is converted to kbps internally.
- Egress & Ingress Limiting: Applies TC rules for egress (upload) directly on your selected interface, and for ingress (download) by redirecting traffic to the ifb0 virtual interface.
- Easy Limit Management: Apply or clear limits with a single click.
- Debian Packaging: Packaged for easy installation on Debian-based systems.

Installation

A Debian package (.deb) is provided for easy installation on Debian-based systems.

1. Install the Package:

   sudo dpkg -i traffic-limiter_1.0.deb

2. Launch the Application:

   You can now launch Traffic Limiter either by running:

   traffic-limiter

   or from your desktop application menu.

Usage

1. Select an Interface:  
   The application displays all available network interfaces along with their IP addresses. Select the desired interface from the list.

2. Set Bandwidth Limits:  
   Choose the desired unit (B/s, KiB/s, MiB/s) and enter a numeric value. The value will be converted to kbps for internal processing.

3. Apply Limits:  
   Click the "Apply Limit" button. The program will:
   - Set an egress limit directly on the selected interface.
   - Automatically load the ifb module, bring up ifb0, and redirect ingress traffic to it.
   - Apply a matching TBF rule on ifb0 for ingress limiting.

4. Clear Limits:  
   Click the "Clear Limit" button to remove any active TC rules from both the selected interface and ifb0.

Notes

- Permissions: Traffic Limiter uses sudo to execute tc commands; ensure your user has appropriate permissions.
- IFB Module: The application automatically loads the ifb module and configures ifb0. Any benign error messages (like "Cannot delete qdisc with handle of zero") can be safely ignored.
- Debian Systems: The package is built and tested on Debian-based distributions. Other systems may require additional configuration.

License

Traffic Limiter is licensed under the GNU General Public License v3 (GPLv3). See the LICENSE file for the full license text.
